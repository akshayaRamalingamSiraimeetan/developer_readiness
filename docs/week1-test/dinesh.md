# Week 1 Test

**Name:** [dinesh]
**Team:** [developer]

## What I learned this week

- **Git/GitHub:**
- **JavaScript:**
- **Expo:**
- **Neuronest:**

## One thing I am still confused about

- How to handle merge/rebase conflicts properly when working with Git. and working to improve on it

## One thing I think I can contribute to the project

- I can help with implementing features, fixing bugs, and testing the project

## PART 2 — Git/GitHub Questions

1. What is the difference between `git` and GitHub?
   git is a version control system, and tracks changes in code.
   github is an online platform for hosting git repositories and runs on internet for storing repositories online

2. What is a branch and why are we using separate branches instead of working directly on `main`?
   A branch is a seperate line of development to work on changes without affecting the main branch.
   we use seperate branches allowing multiple people to work on same/different elements of code and it makes testing easier.
   branching is also helpful to undo unnecesary part of the element or code

3. What does this do?

   ```bash
   git pull origin main
   ```

   This command downloads latest changes from main branch on github and megers it into current local branch

4. What is the difference between:
   - `git add .`
   - `git commit`
   - `git push`

   `git add .` => takes changed/new files and puts them into staging area
   `git commit` => saves the staged changes as permenant snapshot in local git repository
   `git push` => uploads local commits to remote repository such as github

5. What is a Pull Request?
   A pull request is a request to merge the changes from one branch to main/another branch

6. Why shouldn't you directly push to `main` in our project?
   We should not directly push to main because it is the stable branch. Working on separate branches allows code review, testing, conflict prevention, and protects the main project from broken or unfinished code.
7. What would you do if you start working on a task and someone else has already pushed changes to `main`?
   I would not overwrite their changes. I would pull the latest changes from main, merge them into my branch, resolve any conflicts and then push my branch and create a Pull Request.

8. What makes a good commit message? Give two examples.
   A good commit message should be clear, and describe exactly what change was made.
   examples
   Added login validation
   Fixed database connection error

## PART 3 — JavaScript Basics

### 1. Variables

What is the difference between:

- `let`
- `const`
- `var`

Which ones would you normally use in our project?

let and const have block scope but var has function scope
let and const dont suuport redeclaration so its afer to use them in the project

### 2. Functions

What is the difference between:

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

the first function is a general function declaration in older versions of javascript
the second function is an arrow function used in modern javascript
and arrow function cant be called before declaration
arrrow functions are better to use for common callbacks and short functions

### 3. Arrays

What will this produce?

```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.map((n) => n * 2);
```

map() goes through each element of the array and creates a new array.
in this example it is [2,4,6,8]

### 4. map, filter, find

Explain what these do:

- `map()`
- `filter()`
- `find()`

Give one simple example of each.

map() changes each element and returns a new array.
ex const numbers = [1, 2, 3, 4];

const result = numbers.map(n => n + 2);

console.log(result);
[3, 4, 5, 6]

filter() selects elements that satisfy a condition and returns a new array.
ex
const numbers = [1, 2, 3, 4, 5];

const result = numbers.filter(n => n > 2);

console.log(result);
[3, 4, 5]

find() returns the first element that satisfies a condition.
ex
const numbers = [1, 2, 3, 4, 5];

const result = numbers.find(n => n > 2);

console.log(result);
3

### 5. Objects

What does this represent?

```javascript
const child = {
  name: "Alex",
  age: 8,
  interests: ["drawing", "music"],
};
```

How would you access the child's name?
This represents a object that stores information about a child.
can access the childs name using dot notation -- child.name
or bracket notation child["name"]

### 6. Destructuring

What does this do?

```javascript
const { name, age } = child;
```

t takes the name and age properties from the child object and puts them into separate variables.

### 7. Async/Await

What is the purpose of:

- `async`
- `await`

Why would we need them when communicating with a backend/API?

async and await are used to handle asynchronous operations, such as communicating with a backend/API.
await tells JavaScript to wait for a Promise to finish before continuing to the next line inside that async function.
fetch() sends a request to the backend.
await waits for the response.
response.json() converts the response into JavaScript data.
We can then use the data.

### 8. API

Suppose the backend gives us: `GET /api/children`

What do you think this endpoint is used for?

GET /api/children is an API endpoint used to retrieve information about children from the backend.
GET We want to retrieve/read data.
api Indicates that this is an API route.
children Refers to the collection of children.

## PART 4 — React / Expo Basics

### 1. What is React?

Explain in your own words what React is used for.

React is a JavaScript library used to build user interfaces for web applications.
it is useful to create reusable components to efficiently update ui when data changes

### 2. What is a component?

What do you think this means?

```javascript
function Welcome() {
  return <Text>Hello!</Text>;
}
```

A component is a reusable block of a React application.
in this example welcome is a component and can be used repeatedly

### 3. State

What is `useState()` used for?

Give one example where we might use state in Neuronest.

useState() is a React Hook used to store data that can change while the app is running.
When the state changes, React re-renders the component so the UI shows the updated value.
in nueronest app we could use it to store currently selected screen and update the screen when user selects different screen

### 4. Props

What are props in React?
Props are used to pass data from one React component to another
ex <childcard name = "Alex" age{10}> here name is prop

### 5. Expo

What is Expo and why are we using it?
Expo is a framework and set of tools built around React Native that makes it easier to develop and run mobile applications.

### 6. Running the project

What command would you use to start an Expo development server?

What is the purpose of: `npx expo start`
npx expo start starts the Expo development server for our React Native project. after running it we can us android/ios simulator or android phone

### 7. Platform

Why might we use Expo/React Native instead of building completely separate Android and iOS applications?
We use Expo/React Native because it allows us to build an application for both Android and iOS using mostly the same codebase.
this reduces the development time and avoids code duplication

## PART 5 — Team Workflow

You are assigned: "Implement the login screen."

What would you do before starting?

i would first understand th requirments and the existing project structure like what fields are needed like email username andd password etc
i would check the existing components and check whether already an auth code already exists

### Scenario 2

You are working on your branch and someone else has merged changes into `main`.

What should you do before opening your PR?

I should make sure my branch contains the latest changes from main before opening pr
if there are merge conflicts i would resolve them according to the necessities and requirments and test the project

### Scenario 3

You get a merge conflict.

What does that mean? What would you do?

i would open the conflicted file and decide which should be kept according top requirments and having a meeting with the person who did it then resolve it and commit the final resolution

### Scenario 4

You haven't been assigned a development task yet.

What should you be doing during this week?
i will use the time to learn the parts im not exactly comfortable with and understand the project features and what are needed and what are already there like components etc.
