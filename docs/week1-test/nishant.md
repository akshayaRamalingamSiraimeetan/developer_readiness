# Week 1 Test

**Name:** Nishant singh
**Team:** desktop development 

## What I learned this week

- **Git/GitHub: revised the basic commands and new technique** 
- **tailscale: not related to the porject but i improved my skills in tailscale** 
- **Expo: expo SDK 57** 
- **live app animation: learned the integration part of the animations and mascot in app like dualingo** 


## Part 2 — Git/GitHub Questions

### 1. What is the difference between git and GitHub?

Git is a version control system used to track changes in code locally. GitHub is an online platform that hosts Git repositories and provides collaboration features such as Pull Requests and code reviews.

### 2. What is a branch and why are we using separate branches instead of working directly on main?

A branch is a separate line of development. We use separate branches so developers can work independently without directly affecting main. This also allows changes to be reviewed through Pull Requests before being merged.

### 3. What does `git pull origin main` do?

It downloads the latest changes from the main branch of the remote repository named origin and integrates them into the current local branch.

### 4. What is the difference between git add ., git commit, and git push?

- `git add .` stages the changes for a commit.
- `git commit` saves the staged changes as a checkpoint in local Git history.
- `git push` uploads local commits to the remote GitHub repository.

### 5. What is a Pull Request?

A Pull Request is a request to merge changes from one branch into another. It allows other developers to review the changes before they are merged.

### 6. Why shouldn't you directly push to main in our project?

Directly pushing to main can introduce bugs or unreviewed changes. Using branches and Pull Requests provides code review and protects the main branch.

### 7. What would you do if you start working on a task and someone else has already pushed changes to main?

I would update my branch with the latest changes from main, resolve any conflicts if necessary, test my changes, and then continue with my Pull Request.

### 8. What makes a good commit message? Give two examples.

A good commit message is short, specific, and clearly describes what changed.

Examples:
- `Add login screen`
- `Fix API authentication error`


## PART 3 — JavaScript Basics

### 1. Variables

`let` is used when a variable may need to be reassigned.

`const` is used when a variable should not be reassigned.

`var` is the older way of declaring variables and is generally avoided in modern JavaScript because of its scoping behavior.

I would normally use `const` by default and `let` when the value needs to be reassigned.

### 2. Functions

Both examples create a function that adds two numbers.

The first uses a traditional function declaration:

    function add(a, b) {
        return a + b;
    }

The second uses an arrow function:

    const add = (a, b) => {
        return a + b;
    };

Both perform the same operation in this example. Arrow functions are commonly used in modern JavaScript, especially for callbacks.

### 3. Arrays

The result will be:

    [2, 4, 6, 8]

The `map()` function creates a new array by multiplying each number by 2.

### 4. map, filter, find

`map()` creates a new array by transforming every element.

Example:

    const doubled = [1, 2, 3].map(n => n * 2);

Result:

    [2, 4, 6]

`filter()` creates a new array containing only the elements that satisfy a condition.

Example:

    const even = [1, 2, 3, 4].filter(n => n % 2 === 0);

Result:

    [2, 4]

`find()` returns the first element that satisfies a condition.

Example:

    const result = [1, 2, 3, 4].find(n => n > 2);

Result:

    3

### 5. Objects

The object represents a child with a name, age, and list of interests.

    const child = {
        name: "Alex",
        age: 8,
        interests: ["drawing", "music"]
    };

The child's name can be accessed using:

    child.name

This returns:

    "Alex"

### 6. Destructuring

    const { name, age } = child;

This extracts the `name` and `age` properties from the `child` object and stores them in separate variables.

After destructuring, `name` contains `"Alex"` and `age` contains `8`.

### 7. Async/Await

`async` is used to define a function that performs asynchronous operations.

`await` waits for an asynchronous operation, such as an API request, to complete before continuing.

They are useful when communicating with a backend/API because network requests take time to complete and are asynchronous.

Example:

    async function getChildren() {
        const response = await fetch("/api/children");
        const data = await response.json();
        return data;
    }

### 8. API

`GET /api/children` would typically be an API endpoint used to retrieve a list of children from the backend.

## PART 4 — React / Expo Basics

### 1. What is React?

React is a JavaScript library used to build user interfaces. It allows developers to create reusable components and efficiently update the UI when data changes.

### 2. What is a component?

A component is a reusable part of a user interface.

For example:

    function Welcome() {
        return <Text>Hello!</Text>;
    }

Here, `Welcome` is a React component that returns a piece of UI displaying "Hello!".

### 3. State

`useState()` is a React Hook used to store and update data that can change over time inside a component.

For example, in Neuronest, we could use state to store the currently selected child, the loading status of a screen, or whether a menu is open.

### 4. Props

Props are values passed from a parent component to a child component. They allow components to receive data and make components reusable.

For example, a parent component could pass a child's name to a child component as a prop.

### 5. Expo

Expo is a framework and development platform for React Native. It provides tools that make it easier to develop, test, run, and build mobile applications for Android and iOS.

We use Expo because it simplifies the React Native development workflow and allows much of the same code to be used across platforms.

### 6. Running the project

The command used to start an Expo development server is:

    npx expo start

The purpose of `npx expo start` is to start the Expo development server and provide options to run the application on a physical device, Android emulator, or iOS simulator.

### 7. Platform

We might use Expo and React Native instead of building completely separate Android and iOS applications because much of the code can be shared between both platforms.

This reduces development time, avoids duplicating code, and makes the application easier to maintain.

## PART 5 — Team Workflow

### Scenario 1

Before starting the login screen, I would first understand the requirements and expected behavior. I would check the existing project structure and look for any existing authentication code, UI components, designs, or API requirements that I can use.

I would make sure my local `main` branch is up to date and then create a separate feature branch for the login screen.

After implementing the feature, I would test it locally and create a Pull Request when it is ready for review.

### Scenario 2

If someone else has merged changes into `main` while I am working on my branch, I would update my local `main` branch and bring the latest changes into my feature branch before opening my Pull Request.

I would resolve any merge conflicts if necessary, test the application, and push the updated branch.

This ensures that my Pull Request is based on the latest version of `main`.

### Scenario 3

A merge conflict happens when Git cannot automatically combine changes because different branches have modified the same part of a file in incompatible ways.

I would inspect the conflicting files, understand both changes, resolve the conflict appropriately, remove the conflict markers, and test the application.

After resolving the conflict, I would commit the resolution and push the branch again.

### Scenario 4

I should not simply wait for a development task.

I would use the time to set up and explore the project, understand the existing architecture and codebase, review the README and existing issues, learn the technologies being used, and identify areas where I could contribute.

I would also communicate with the team and ask where I could help if I found something that needed attention.

## Completion

I will commit my completed assessment to my branch, push the branch to GitHub, open a Pull Request, request a review, and wait for the review without merging the Pull Request myself.




