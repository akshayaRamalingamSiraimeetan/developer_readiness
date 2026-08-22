# Week 1 Test

**Name:** [Laitadithya Kariyam]
**Team:** [Develeopment team for tablet/Developer]

## What I learned this week

- **Git/GitHub: Major workflow of git and github with all the basics and fundementals required to use git in the project** 
- **JavaScript: The basics and fundementals of the language and also its use in the project** 
- **Expo: The basic workflow expo along with react to get started with coding using react native** 
- **Neuronest: The idea of neruronest itself and also what type of team work flow is generally expected**

## One thing I am still confused about

- The backend part of the project. (supabase)

## One thing I think I can contribute to the project

-  I can contribute by taking up development tasks as I get familiar with project structure 
   and tools that I am going to use. I can also try to help other team members if they need any.



## My answers:

## Part 1:

1. Clone the repository
    (a) What `git clone` does

    Clones (makes a copy of) a selected remote repository to the local machine to selected folder.
    A feature of distributed vcs. 

    (b) Difference between a local repository and the GitHub repository

    A github repository is hosted on cloud so it can be viewed on the web directly by any user.
    A local repo is a repo present in a local machine itself. Available only to the local user.


2. Create a branch

    Created a branch from latest commit available on remote. Did'nt disturb main branch.


3. Make a small change     

    Created 2 files lalit.md and answers.md (initially blank). Added template text to lalit.md .


4. Commit your changes

    Committed 1st commit with message "Added blank files" on lalit-week1-test branch.


5. Push your branch

    Pushed branch (lalit-week1-test) to remote repo (developer-readiness).


6. Create a Pull Request    

    Created a pull request on GitHub to get my branch merged (through review) with main.


##  Part 2: 

1. What is the difference between `git` and GitHub?

    git is a version control system and github (implemented with git) is a cloud platform for developers to store and share projects or code.



2. What is a branch and why are we using separate branches instead of working directly on `main`?


    branches are sperate pointers instead of main used to diverge from main and make independent commits. Generally main is considered to have only the production ready commits and so working directly on main is not advised.


3. What does this do? git pull origin main

    This command fetches all the reachable history on the remote main branch and updates origin/main (local reference). Then it merges that origin/main with our current active branch.



4. What is the difference between:- `git add .` - `git commit` - `git push`  

    git add . -> adds all untracked or modifed files to staged area where it is ready to get committed.

    git commit -> commits staged changes as an accessable version of our files. commits can created on any branch.

    git push -> pushes our selected branch into the remote repo. EX: git push origin main


5. What is a Pull Request?

    A pull request is a request to merge a branch to main and create a merged commit on main where it would have both features of main and the branch.

6. Why shouldn't you directly push to `main` in our project?

    Main is considered to have production ready code (working versions of our code). So pushing to main is not advisable as some unwanted commits might get pushed.


7. What would you do if you start working on a task and someone else has already pushed changes to `main`?

    First I would fetch the remote repo and veiw the changes. Then accoriding to the changes i would then merge it to my current branch. I try  to use this more often pulling directly.

8. What makes a good commit message? Give two examples.

    A good commit message should be something which accuratly describes all changes made in that commit in one single phrase.

        Ex : Added a new resgistration/login page , Added a new settings menu 




## PART 3 — JavaScript Basics 


1. What is the difference between: `let` `const` `var`

Which ones would you normally use in our project?

    let allows to define a variable and that variables value can be re-assigned . Whereas for const u can declare the variable but cannot re-assign to the variable. 
    var is legacy way of defining a variable on javasrcipt . Can be used to redefine or reassign but is droped in modern js use because it is function scoped.
    I would use let and const in our project as they are flexible by themselves and only use var if absolutely necessary.


2. What is the difference between:  
```javascript
function add(a, b) {
    return a + b;
}
```

and:

```javascript
const add = (a, b) => {
    return a + b;
}; 
```

    Both are ways of defining a function but a few differences. The main difference is that arrow function uses the 'this' variable in itself as its surrounding context and not as which object is calling it. Also they dont have there own 'arguements' and  use rest parameters instead to group arguements if needed.

3. Arrays

What will this produce?

```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.map(n => n * 2);
```
    
    goes through every element and return's element multiplied with 2 to result array and hence store all elements multiplied with 2. so result will be [2, 4, 6, 8] . 


4. map, filter, find

Explain what these do:
- `map()`
- `filter()`
- `find()`

Give one simple example of each.

    numbers = [2,4,6,8]
    
    result = numbers.map(n => n/2);      result = [1,2,3,4]
    result = numbers.filter(n => n % 4 == 0);       result = [4,8]
    result = numbers.find(n => n>3);       result = 4 


5. What does this represent? How would you access the child's name? 

```javascript
const child = {
    name: "Alex",
    age: 8,
    interests: ["drawing", "music"]
};
```
    this is a typical object in javascript. The name can be accessed using child.name .


6. Destructuring

What does this do?

```javascript
const { name, age } = child;
```


    it assign's values to name and age if child has the same attribute name's. Hence it is flexible because we can access specific members using a single sentence.


7. Async/Await

What is the purpose of:
- `async`
- `await`

Why would we need them when communicating with a backend/API?  


    A backend or API might take sometime before they actually respond back to the userinterface(frontend). So using fetch ()returns a promise to fetch some response. So for this case async function with await pauses that function till response is recieved so someother code can we executed in the mean time.


8. API

Suppose the backend gives us: `GET /api/children`

What do you think this endpoint is used for?

    This endpoint might be used to retreive data (get method) about children.


## PART : 4

1. What is React?

Explain in your own words what React is used for.


    React is a frontend library used to model a frontend project. Unlike a framework where the base structure is alrdy defined you use react as a library(its tools) to create interactive and reusasble UI, leaving the strucuture of the project in the hands of the developer.

 2. What is a component?

What do you think this means?

```javascript
function Welcome() {
    return <Text>Hello!</Text>;
}
```

    A component is a resuable block of the code that defines and adds logic to a peice of UI. The above is a function component which returns a text block and displays on the UI.

3. What is `useState()` used for?

Give one example where we might use state in Neuronest.

    useState is used to re-render a component using state variable changes (when state changes the component gets re-rendered).
    it is useful in the app when the user clicks a button, accordingly we can animate speacial parts of the screen which make it moer interactive.

4. Props

What are props in React?

    props are attributes of components which can be assigned some value to design the component as we wish.


5. Expo
What is Expo and why are we using it?    
 

    Expo is a framework built around react native which is used to develop apps without having to code the functionalty of the app from the very start. It makes developing react native apps much easier with its tools and libraries etc.
    Works for both iOS and Android so it supports multi platform. For this project as we want to implement in both iOS and Android we can use expo to develop for both platforms simutaneously without worrying about platform specific problems.

6. Running the project

What command would you use to start an Expo development server?

What is the purpose of: `npx expo start`


    I would use npx expo start or npx expo start --android (for android studio) to start development server.
    npx is a package command executer. Here in npx expo go it executes command in expo package to start the development server.

7. Platform

Why might we use Expo/React Native instead of building completely separate Android and iOS applications?


    To reduce needs for constantly worrying about platform specific development/configuration , we use expo(react native). It significantly reduces effort required to develop a cross platform app as it a framework supported both on iOS and android

## PART 5 


Scenario 1

You are assigned: "Implement the login screen."

What would you do before starting?

    First I would discuss with the team about all the requirements and process to implement the login screen. Before starting to code it I would use git fetch and then merge to my branch for any latest commits/updates which might not be present on my system.

    
    
Scenario 2

You are working on your branch and someone else has merged changes into `main`.

What should you do before opening your PR?

    Before opening my PR, I would make sure my branch is up to date with main by fetching the latest changes and merging or rebasing them into my branch. I would then resolve any merge conflicts, test my changes, and make sure everything works before opening the PR.
    

Scenario 3

You get a merge conflict.

What does that mean? What would you do?

    Getting a merge conflict is normal. It means the two histories that are trying to get merged have changes in same part of a file.
    Hence we have to discuss with the team on what changes to be kept for the final merged commit.



Scenario 4

You haven't been assigned a development task yet.

What should you be doing during this week?

**Note:** The expected behavior is NOT "Wait until you are given a task."


    I would look to learn more about the project like more about the project itself or learning more about the tech stack in the free or spare time im getting. Other than that i would also try to help other team members with thier tasks if they require any help.

