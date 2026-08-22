# Week 1 Test

**Name:** Badhrinath Nagidi
**Team:** Tablet APP Development Team

## What I learned this week

- **Git/GitHub:** I learned how to clone a repository, create branches, stage changes, commit changes, and connect my local repository with GitHub.
- **JavaScript:** I learned the basics of variables, functions, arrays, objects, map(), filter(), find(), and async/await.
- **Expo:** I learned that Expo is used with React Native to develop and test mobile applications.
- **Neuronest:** I learned about the project's development workflow and how the frontend, backend, APIs, and mobile application can work together.

## One thing I am still confused about

- I am still learning how React Native, Expo, and the backend API communicate with each other in a complete application , I mean how API is going to work.

## One thing I think I can contribute to the project

- Initially I had made some projects , so I have a little bit experience of doing it , just the language and platform is changed . So I think I can contribute in Frontend development and also Backend for the APP.

# Part 2 — Git/GitHub Questions

## 1. What is the difference between Git and GitHub?

Git is a version control system that is used to track changes in code and manage different versions of a project. GitHub is an online platform where Git repositories can be stored, shared, and collaborated on with other developers.

## 2. What is a branch and why are we using separate branches instead of working directly on main?

A branch is a separate line of development in a Git repository. We use separate branches so that each developer can work on their own task without affecting the main branch. After completing the work, the changes can be reviewed through a Pull Request before being merged into main.

## 3. What does `git pull origin main` do?

It gets the latest changes from the main branch of the remote repository named origin and integrates those changes into the current branch.

## 4. What is the difference between `git add .`, `git commit`, and `git push`?

- `git add .` stages the changes so they are ready to be committed.
- `git commit` saves the staged changes as a commit in the local Git repository.
- `git push` uploads the local commits to the remote GitHub repository.

## 5. What is a Pull Request?

A Pull Request is a request to merge changes from one branch into another branch. It allows other team members to review the code before it is merged.

## 6. Why shouldn't you directly push to main in our project?

We should not directly push to main because it is the shared branch of the project. Direct changes could introduce bugs or unfinished code. Using branches and Pull Requests allows the team to review changes before they are merged.

## 7. What would you do if you start working on a task and someone else has already pushed changes to main?

I would first update my local information about main and bring the latest changes into my branch. I would resolve any conflicts if they occur, test my work again, and then create the Pull Request.

## 8. What makes a good commit message? Give two examples.

A good commit message should clearly and briefly describe what was changed.

Examples:
- `Add week 1 developer assessment`
- `Fix login form validation`

# Part 3 — JavaScript Basics

## 1. Variables

`let`, `const`, and `var` are used to declare variables in JavaScript.

- `let` is used when the value may need to change.
- `const` is used when the variable will not be reassigned.
- `var` is the older way of declaring variables and has different scoping behavior.

In our project, I would normally use `const` by default and `let` when the value needs to change. I would generally avoid `var` in modern JavaScript.

## 2. Functions

Both of these are used to create functions.

```javascript
function add(a, b) {
    return a + b;
}
```

This is a normal function declaration.

```javascript
const add = (a, b) => {
    return a + b;
};
```

This is an arrow function. Both functions take `a` and `b` as inputs and return their sum. The main difference here is the syntax used to define them.

## 3. Arrays

```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.map(n => n * 2);
```

The result will be:

```javascript
[2, 4, 6, 8]
```

`map()` goes through every element of the array and creates a new array using the returned value.

## 4. map, filter, find

### map()

`map()` transforms every element of an array and returns a new array.

```javascript
const numbers = [1, 2, 3];
const result = numbers.map(n => n * 2);
// [2, 4, 6]
```

### filter()

`filter()` returns a new array containing only the elements that satisfy a condition.

```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.filter(n => n > 2);
// [3, 4]
```

### find()

`find()` returns the first element that satisfies a condition.

```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.find(n => n > 2);
// 3
```

## 5. Objects

```javascript
const child = {
    name: "Alex",
    age: 8,
    interests: ["drawing", "music"]
};
```

This represents an object called `child` containing information about a child, such as name, age, and interests.

The child's name can be accessed using:

```javascript
child.name
```

This gives:

```text
Alex
```

## 6. Destructuring

```javascript
const { name, age } = child;
```

This extracts the `name` and `age` properties from the `child` object into separate variables.

It is a shorter way of writing:

```javascript
const name = child.name;
const age = child.age;
```

## 7. Async/Await

`async` and `await` are used to work with asynchronous operations.

`async` is used to define an asynchronous function, and `await` is used inside an async function to wait for a Promise to complete before continuing.

For example:

```javascript
async function getChildren() {
    const response = await fetch("/api/children");
}
```

We need this while communicating with a backend/API because sending a request and receiving a response can take some time.

## 8. API

If the backend provides:

```text
GET /api/children
```

I think this endpoint is used to request and retrieve children data from the backend.

For example, the backend may return information such as the children's names, ages, or other details, which the application can then use or display.


# Part 4 — React / Expo Basics

## 1. What is React?

React is a JavaScript library used to build user interfaces. It allows developers to create reusable components and manage the user interface of an application.

## 2. What is a component?

A component is a reusable part of a user interface.

For example:

```javascript
function Welcome() {
    return <Text>Hello!</Text>;
}
```

Here, `Welcome` is a component that displays the text `Hello!`. Components help us divide an application into smaller and reusable parts.

## 3. State

`useState()` is used to store and manage data that can change inside a React component.

For example:

```javascript
const [count, setCount] = useState(0);
```

Here, `count` is the current state and `setCount` is used to update the state.

In Neuronest, we could use state for things such as login information, form input, selected child information, or loading status.

## 4. Props

Props are values or information passed from one React component to another component.

For example:

```javascript
<Welcome name="Badhrinath" />
```

Here, `name` is a prop passed to the `Welcome` component.

Props make components reusable because the same component can receive different values.

## 5. Expo

Expo is a development platform and set of tools used with React Native. It makes it easier to develop, run, test, and build mobile applications for Android and iOS.

We are using Expo because it provides tools that make React Native mobile app development easier.

## 6. Running the project

The command used to start an Expo development server is:

```bash
npx expo start
```

This starts the Expo development server and provides options to run and test the application on a device or emulator.

## 7. Platform

We might use Expo and React Native instead of building completely separate Android and iOS applications because React Native allows us to share much of the code between both platforms.

This can reduce development time and avoid writing the same application separately for Android and iOS.

