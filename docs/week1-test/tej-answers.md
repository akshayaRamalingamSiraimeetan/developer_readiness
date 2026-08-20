# Week 1 Developer Readiness Assessment -> Parts 2 to 5

**Name:** Ramcharan Tej
**Team/Role:** Mobile/Tablet Developer

# PART 2 -> Git/GitHub Questions

## 1. What is the difference between Git and GitHub?

Git is a version control system that is used to track changes in a project. It runs locally on my computer and allows me to create commits and branches.

GitHub is an online platform where Git repositories can be stored and shared. It also provides features such as Pull Requests, code reviews and collaboration.

In simple terms, Git manages the version history of the code, while GitHub provides an online place to store and collaborate on the repository.

## 2. What is a branch and why are we using separate branches instead of working directly on `main`?

A branch is a separate line of development in a Git repository.

We use separate branches so that each developer can work on their assigned task without directly changing `main`.

This helps because:

* Developers can work on different tasks independently.
* Changes can be reviewed before being merged.
* Problems in a feature branch do not immediately affect `main`.
* It makes team collaboration safer.

## 3. What does this do?

bash
git pull origin main


This gets the latest changes from the `main` branch of the remote repository called `origin` and integrates them into my current local branch.

It is useful when other developers have already pushed changes to `main` and I need those changes in my branch.

## 4. What is the difference between `git add .`, `git commit`, and `git push`?

### `git add .`

This stages the changed files so Git knows which changes should be included in the next commit.

bash
git add .


### `git commit`

This saves the staged changes in the local Git history.

bash
git commit -m "Add week 1 assessment"


### `git push`

This uploads my local commits to the remote GitHub repository.

bash
git push


The general workflow is:

text
Make changes -> git add . -> git push -> GitHub

## 5. What is a Pull Request?

A Pull Request is a request to merge changes from one branch into another branch.

For example:

text
tej-week1-test -> main


The team can review the changes, provide feedback and check the work before it is merged into `main`.

## 6. Why shouldn't you directly push to `main` in our project?

I should not directly push to `main` because the main branch should remain stable.

Using a separate branch and Pull Request allows the team to:

* Review the code.
* Test the changes.
* Give feedback to the code.
* Find problems before merging the code.
* Work on different tasks without interfering with each other in the task.

## 7. What would you do if you start working on a task and someone else has already pushed changes to `main`?

I would first make sure my current work is saved or committed.

Then I would get the latest changes from `main` and update my branch.

For example:

bash
git fetch origin
git checkout main
git pull origin main
git checkout my-branch
git merge main


If there are merge conflicts, I would resolve them, test the application and then push the updated branch.

## 8. What makes a good commit message? Give two examples.

A good commit message should be short, clear and describe what was changed.

Examples:

Add login screen

Fix child profile navigation

# PART 3 -> JavaScript Basics

## 1. Variables

### `let`

`let` is used when the value of a variable may change.

let score = 10;

score = 20;


### `const`

`const` is used when the variable should not be reassigned.


const name = "Tej";


### `var`

`var` is the older way of declaring variables in JavaScript. It has different scoping behavior from `let` and `const`.

In a modern project, I would normally use `const` and `let` and avoid using `var` unless there is a specific reason.

## 2. Functions

The first example is a normal function:

function add(a, b) {
    return a + b;
}

The second example is an arrow function:

const add = (a, b) => {
    return a + b;
};

Both functions can be called like this:

add(2, 3);

The result is: 5

The main difference is the syntax. Arrow functions are commonly used in modern JavaScript and React code.



## 3. Arrays

Given:


const numbers = [1, 2, 3, 4];

const result = numbers.map(n => n * 2);


`map()` applies the given function to every element in the array.

Therefore:

result

produces:

[2, 4, 6, 8]



## 4. `map()`, `filter()`, and `find()`

### `map()`

`map()` creates a new array by transforming every element.

const numbers = [1, 2, 3];

const result = numbers.map(n => n * 2);


Result:

[2, 4, 6]


### `filter()`

`filter()` creates a new array containing the elements that satisfy a condition.


const numbers = [1, 2, 3, 4];

const result = numbers.filter(n => n > 2);


Result:

[3, 4]


### `find()`

`find()` returns the first element that satisfies a condition.

const numbers = [1, 2, 3, 4];

const result = numbers.find(n => n > 2);


Result:

3



## 5. Objects

This represents an object containing information about a child:

const child = {
    name: "Alex",
    age: 8,
    interests: ["drawing", "music"]
};


The object contains three properties:

* `name`
* `age`
* `interests`

The child's name can be accessed using:

child.name

The result is:

Alex


## 6. Destructuring

Given:

const { name, age } = child;


This extracts the `name` and `age` properties from the `child` object and creates variables with those names.

It is similar to writing:


const name = child.name;
const age = child.age;


but destructuring allows both values to be extracted in one statement.

## 7. Async/Await

`async` and `await` are used when working with asynchronous operations.

For example, when communicating with a backend API, the application has to wait for a response.


async function getChildren() {
    const response = await fetch("/api/children");
    const data = await response.json();

    return data;
}


`async` makes a function asynchronous.

`await` waits for an asynchronous operation to complete before continuing.

They make asynchronous code easier to read and understand.

## 8. API

If the backend provides:

text
GET /api/children


I would expect this endpoint to retrieve information about children from the backend.

For example, it could return:


[
    {
        name: "Alex",
        age: 8
    },
    {
        name: "Sam",
        age: 9
    }
]


`GET` is normally used to request data from the backend.

# PART 4 -> React / Expo Basics

## 1. What is React?

React is a JavaScript library used to build user interfaces using reusable components.

In our project, React is used to create the different parts of the application's user interface.

## 2. What is a component?

A component is a reusable part of a React application.

For example:


function Welcome() {
    return <Text>Hello!</Text>;
}


Here, `Welcome` is a React component.

When it is rendered, it displays:

text
Hello!


Components help divide an application into smaller and reusable parts.

## 3. State

`useState()` is a React Hook used to store information that can change while the application is running.

For example:


const [score, setScore] = useState(0);


Here:

* `score` is the current state value.
* `setScore` is used to change the value.
* `0` is the initial value.

In Neuronest, state could be used for information such as the currently selected child, information entered into a form or the current screen data.

## 4. Props

Props are values passed from a parent component to a child component.

For example:


function Welcome({ name }) {
    return <Text>Hello {name}</Text>;
}


The parent can pass a value:


<Welcome name="Alex" />


The `Welcome` component receives `"Alex"` through the `name` prop.

Props allow components to receive data and be reused with different values.

## 5. Expo

Expo is a development platform and set of tools used with React Native.

We use Expo to make React Native development and testing easier.

It provides tools that help us run and develop the mobile application during development.

## 6. Running the project

The command used to start an Expo development server is:

bash
npx expo start


This starts the Expo development server and provides options for running and testing the application.

Depending on the project setup, the application can then be tested using a device, emulator or other supported development environment.

## 7. Platform

We can use Expo and React Native instead of building completely separate Android and iOS applications because React Native allows us to share much of the application code between platforms.

This can:

* Reduce duplicated code.
* Reduce development time.
* Make maintenance easier.
* Allow the same application logic to be used across platforms.

# PART 5 -> Team Workflow

## Scenario 1 -> You are assigned: "Implement the login screen."

Before starting, I would first understand what the task requires.

I would:

1. Read the task or issue description.
2. Understand the expected login functionality.
3. Check the existing project structure.
4. Check whether authentication or UI components already exist.
5. Check whether another developer is working on the same feature.
6. Make sure my local repository is up to date.
7. Create a separate branch for the login task.
8. Implement the feature.
9. Test the feature locally.
10. Commit my changes with a meaningful commit message.
11. Push my branch.
12. Create a Pull Request for review.

I would not directly modify `main`.

## Scenario 2 -> You are working on your branch and someone else has merged changes into `main`.

I would update my branch with the latest changes from `main` before opening my Pull Request.

First, I would make sure my current work is saved and committed.

Then I would run:

bash
git fetch origin
git checkout main
git pull origin main
git checkout my-branch
git merge main


If there are conflicts, I would resolve them and test the application.

After everything works correctly, I would push my updated branch:

bash
git push


Then I would open my Pull Request.

## Scenario 3 -> You get a merge conflict.

A merge conflict happens when Git cannot automatically combine changes from different branches.

For example, two developers may have changed the same lines of a file differently.

I would:

1. Read the conflict carefully.
2. Open the affected file.
3. Identify the conflicting changes.
4. Decide which changes should be kept or combine them if both are required.
5. Remove the conflict markers.
6. Test the application.
7. Stage the resolved files.

For example:

bash
git add .


Then:

bash
git commit -m "Resolve merge conflict"


Finally:

bash
git push


If I am unsure which change should be kept, I would ask the relevant team member instead of guessing.

## Scenario 4 -> You haven't been assigned a development task yet.

I should not simply wait for a task.

I would use the time to understand the project and prepare myself to contribute.

I would:

* Study the NeuroNest project structure.
* Run the application locally.
* Read the existing code.
* Learn the technologies being used.
* Read the project documentation.
* Understand the team's Git workflow.
* Look for areas where I can contribute.

This would help me become familiar with the codebase so that I can start working efficiently when I receive a development task.
