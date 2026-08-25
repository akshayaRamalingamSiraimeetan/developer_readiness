# Week 1 Test

**Name:** Lathikaa J
**Team:** Development Team (Mobile/Tablet version)

## What I learned this week

- **Git/GitHub:** This week I explored and learned the basic git commands , pull requests , cloning repo 
- **JavaScript:** Learnt the basics of Javascript , I still have to learn more of it
- **Expo:** Explored Expo basics and set up the environment for Tablet version since this is my first time doing it 
- **Neuronest:** Went through the Project repository and understood the structure

## One thing I am still confused about

- Since this is my first time working with many people on a single repo , I'm confused about how it will turn out.

## One thing I think I can contribute to the project

- I can contribute to the development part by becoming more familiar with the project structure , expo environment


# Part 2 — Git/GitHub Questions

## 1. What is the difference between Git and GitHub?
- Git is a version control system , used to track the changes in the project that we do locally whereas Github is a platform that contains repositories which can be used by other developers as well and do shared and collaborated work .

## 2. What is a branch and why are we using separate branches instead of working directly on `main`?
- A branch is a separate version of the project in which we can do our code, changes and later push into main. We are using branch instead of working directly on main because , the project may consist of many developers with their own task , which may lead to abrupt code changes in main . Using branch ensures that the code is accessed properly before merging it into main branch. 
## 3. What does this do?

`git pull origin main`
-It downloads the latest changes from the remote main branch and updates my local branch with those changes

## 4. What is the difference between:

- `git add .` - it is used to to stage all the files for next commit
- `git commit`- it saves the staged changes , acts like a checkpoint
- `git push`- it is the acutal command which commits the files to the repo

## 5. What is a Pull Request?
it is a request to review the changes made in one branch before merging them into another branch

## 6. Why shouldn't you directly push to `main` in our project?
Pushing drectly to main can affect the main project. It is best to review and test the branches before merging so that unnoticed errors can be avoided.

## 7. What would you do if you start working on a task and someone else has already pushed changes to `main`?
I would first get the latest changes from main into my local repository and update my branch. Then I would resolve any conflicts if necessary, test my changes, and push my updated branch before opening the Pull Request.

## 8. What makes a good commit message? Give two examples.
 Good commit message should have clear and concise message of what changes we made.

 Eg - Fix API error handling , Update Expo development environment setup
---

# Part 3 — JavaScript Basics

## 1. Variables

What is the difference between `let`, `const`, and `var`?
- let is used for variables , whose values may change 
const is used for variables , its values should not be reassigned 
var is used to declare variables and has different scopes

Which ones would you normally use in our project?

I would normally use const and let in the project. const would be the default, and let would be used when the value needs to change

## 2. Functions

## What is the difference between 

function add(a, b) {
    return a + b;
}

and 

const add = (a, b) => {
    return a + b;
};


- Both the functions does the same task . the first one is regular function and second is arrow 

The difference is arrow functions use smaller syntax which would be helpful for react

## 3. Arrays

What will this produce?

## javascript
const numbers = [1, 2, 3, 4];
const result = numbers.map(n => n * 2);

- [2, 4, 6, 8] will be produced , an array with each number will be multiplied by 2 will be created


## 4. map, filter, find , Give one simple example of each.


map() - transforms every item in an array and returns a new array

eg - const numbers = [1, 2, 3];
const doubled = numbers.map(n => n * 2);
gives -  [2, 4, 6]


filter() - returns all items that match a condition
eg - const numbers = [1, 2, 3, 4];
const even = numbers.filter(n => n % 2 === 0);
gives-  [2, 4]


find() - returns the first item that matches a condition

eg - const numbers = [1, 2, 3, 4];
const result = numbers.find(n => n > 2);
gives - 3

## 5. Objects
What does this represent?

const child = {
    name: "Alex",
    age: 8,
    interests: ["drawing", "music"]
};

- it represents a js object that consists of name , age and interests of a child

How would you access the child's name?

- using child.name will give the child's name

## 6. Destructuring
What does this do?

const { name, age } = child;
- This takes the name and age properties from the child object and stores them directly in separate variables called name and age

## 7. Async/Await

async - it is used to declare a function that performs operation 

await - it pauses the execution until the operation is done 


Why would we need them when communicating with a backend/API?

- because api request take time and we need to wait properly before going to next execution

## 8. API
Suppose the backend gives us: GET /api/children

What do you think this endpoint is used for?
It might be an API endpoint used to request and get  list of children or their data from the backend



## PART 4 — React / Expo Basics

## 1. What is React?
It is a frontend javascript library used for building interactive UI 

## 2. What is a component?

- It is a reusable piece of the user interface

What do you think this means?

function Welcome() {
    return <Text>Hello!</Text>;
}
- It creates a component called Welcome that shows Hello!

## 3. State
What is useState() used for?

- It is used to store and manage data that can change in a component. When the state changes, React updates the component UI accordingly

Eg in Neuronest: We could use state to store the text entered by a user in a login form or to track whether data is loading.


## 4. Props
What are props in React?
- These are the values passed from parent to child component 

For example, a reusable child profile component could receive a child's name as a prop

## 5. Expo
What is Expo and why are we using it?

Expo is a framework and set of tools used to make React native easier . With the help of it we can build , run , test applications easily 

## 6. Running the project
What command would you use to start an Expo development server?

- npx expo start 

What is the purpose of: npx expo start

It starts the Expo development server and provides options to run and test the app on an Android emulator, iOS simulator, or other supported devices

## 7. Platform
Why might we use Expo/React Native instead of building completely separate Android and iOS applications?

Expo/React Native allows us to use a largely shared codebase for Android and iOS instead of building two completely separate applications .This is helpful in saving time and  makes maintaining the application easier



## PART 5 — Team Workflow


## Scenario 1
You are assigned: "Implement the login screen."

What would you do before starting?

- Before starting, I would first understand the task and check the existing project structure and related files. I would pull the latest changes from main, create or use my assigned branch, check whether anyone else is working on related parts, and understand the existing UI and coding structure before making changes.


## Scenario 2
You are working on your branch and someone else has merged changes into main.

What should you do before opening your PR?

I would pull the latest changes from main into my branch, check for any conflicts , test my changes again, and then push the updated branch before opening or updating my Pull Request.

## Scenario 3
You get a merge conflict.

What does that mean? What would you do?
- A merge conflict means Git found conflicting changes that it cannot automatically combine, usually because the same part of a file was changed differently

I would check the conflicting files, understand both changes, decide the correct version with help from the team if needed, resolve the conflict, test the code, and then commit the resolved changes.

## Scenario 4
You haven't been assigned a development task yet.

What should you be doing during this week?

If I haven't been assigned a development task yet, I would go through the project structure, read the existing files, and try to understand the project code better. I would also work on my weak areas and continue learning the required technologies so that I can become more prepared to contribute to the project