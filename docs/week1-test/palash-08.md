# Week 1 Test

**Name:** Palash  
**Team:** [Dev Team]

## What I learned this week

- **Got back on track with JS - cleared up some rusty concepts:**
- **Expo**
- **Neuronest:** Supabase, including Edge Functions and database backups with `pg_dump` through a connection string.
- **FastAPI and data validation:** Pydantic-based data validation... Still learning this one.

## One thing I am still confused about

- Expo, particularly the application-development context and how its tools fit into the workflow.

## One thing I think I can contribute to the project

- As someone with extensive systems administration experience, I can help make the Supabase setup reliable and secure by supporting environment and secret management, access controls, database backups, monitoring, and troubleshooting. I can also contribute to SMTP configuration and delivery.

## Part 2 — Git/GitHub Questions

### 1. What is the difference between Git and GitHub?

Git is the version-control software running locally on my PC... while GitHub works on the same thing but with extra functionality for collaborating with other users and allowing features like PRs, reviews and basically unlocking the doors for OSS

### 2. What is a branch and why use separate branches instead of working directly on `main`?

It helps multiple people work on the same repository. Each dev can have his / her own branch and open a PR to merge it into the main / master branch as required once merge conflicts are resolved. Working directly on the main branch can lead to conflicts, accidental breakage, and a clumsy shared codebase

### 3. What does `git pull origin main` do?

It fetches the latest changes from the remote named origin (conventionally the default remote) on its main branch, then integrates those changes into the current local branch.

### 4. What is the difference between `git add .`, `git commit`, and `git push`?

- `git add .` stages changed and new files for the next commit.
- `git commit` saves the staged changes as a named snapshot in my local Git history.
- `git push` uploads local commits to a branch on the remote repository, such as GitHub.

### 5. What is a Pull Request?

A Pull Request is a request to merge one branch into another. It gives the team a place to review the changes, discuss feedback, and check that the work is ready before it reaches `main`.

### 6. Why should I not directly push to `main` in this project?

`main` is the shared, stable version of the project. Direct pushes could introduce unreviewed changes or break the application for everyone. A branch and Pull Request protect `main` by requiring review and allowing problems to be caught before merging.

### 7. What would I do if someone has already pushed changes to `main`?

I would first save or commit my current work. Then I would fetch the latest `main` branch, merge or rebase those changes into my branch, resolve any conflicts carefully, check if everything works as intended, and then push my updated branch.

### 8. What makes a good commit message? Give two examples.

A good commit message is short, specific, and describes the change rather than the process. For example:

- `feat: implement SMTP email delivery`
- `chore: update development dependencies`
- `add: password-reset screen`


## Part 3 — JavaScript Basics

### 1. Variables

- `const` declares a variable that cannot be reassigned.
- `let` declares a block-scoped variable that can be reassigned
- `var` is the older way to declare variables. It is function-scoped rather than block-scoped and can cause unexpected behaviour (generally avoided in modern JS)

I would normally use `const` by default and `let` when I need to reassign a value.

### 2. Functions

Both examples define a function that adds two values. The first is a function declaration, while the second is an arrow function assigned to a constant. Arrow functions have shorter syntax and handle `this` differently; in React code, they are commonly used for callbacks and small functions. Function declarations are hoisted, while an arrow function stored in `const` cannot be called before it is declared.


### 3. Arrays

`result` will be a new array containing each original value multiplied by two:

```javascript
[2, 4, 6, 8]
```

### 4. `map`, `filter`, and `find`

- map() transforms every item and returns a new array.

  ```javascript
  const doubled = [1, 2, 3].map((number) => number * 2);
  // [2, 4, 6]
  ```

- filter() returns a new array containing only items that meet a condition.

  ```javascript
  const adults = [12, 18, 24].filter((age) => age >= 18);
  // [18, 24]
  ```

- find() returns the first item that meets a condition, or it is undefined if none meet that condition

  ```javascript
  const firstAdult = [12, 18, 24].find((age) => age >= 18);
  // 18
  ```

### 5. Objects

The code represents an object named 'child' containing info about a child: a name, age, and list of interests. The child's name could be accessed with `child.name`.

### 6. Destructuring

```javascript
const { name, age } = child;
```

This extracts the `name` and `age` properties from `child` into separate vars named `name` and `age`...

### 7. Async/Await

`async` marks a function as asynchronous, meaning it returns a Promise. `await` pauses that async function until a Promise is fulfilled and returns its result or throws an error depending on whatever happens

Backend and API requests take time to complete. Using async and await helps in preventing the frontend from stalling - basically it keeps the other processes running and doesn't just stop for THIS specific function call to finish... For example... if a DB query takes too long, the other parts of the code should not just stall

### 8. API

`GET /api/children` could be an endpoint for retrieving data about children from the backend. The application could use the returned data to display child profiles or related information.

## Part 4 — React / Expo Basics

### 1. What is React?

React is a JavaScript library for building user interfaces from reusable components. It helps keep the displayed UI in sync with changing data and user interactions + DOM manipulation + It makes this possible :
Updating a UI component WITHOUT forcing a full page refresh

### 2. What is a component?

A component is a reusable, self-contained part of a React interface. `Welcome` is a component that returns a React Native `Text` element displaying “Hello!”. Components allow an application to be divided into smaller pieces with clear responsibilities.

### 3. State

`useState()` is a React Hook for storing data that can change while a component is running. When its setter updates the state, React re-renders the component with the new value.

### 4. Props

Props are read-only values passed from a parent component to a child component. For example, a reusable child-card component could receive a child's name and age as props, allowing the same component to display different children.

### 5. Expo

Expo is a framework and toolchain built around React Native. We use it to simplify developing, running, testing, and building a mobile app for Android and iOS.

### 6. Running the project

I would start the Expo development server with:

```bash
npx expo start
```

This starts the project’s development server and provides options to run the app on a physical device, emulator, or simulator.

### 7. Platform

Expo and React Native allow the team to share most application code across Android and iOS. This reduces duplicated work, speeds up development, and makes maintenance easier than building two entirely separate native applications.

## Part 5 — Team Workflow

### Scenario 1: I am assigned to implement the login screen. What would I do before starting?

I would first read the task requirements and acceptance criteria, then check the existing project structure for related UI components, authentication logic, API endpoints, and design patterns. I would confirm that nobody else is working on the same files, update my local branch from `main`, create a task-specific branch, and only then begin implementation.

### Scenario 2: Someone has merged changes into `main` while I am working. What should I do before opening my PR?

I would commit or otherwise save my current work, fetch the latest `main`, and merge or rebase it into my branch. If conflicts occur, I would resolve them carefully, test the app again, and then push my updated branch before opening the PR.

### Scenario 3: I get a merge conflict. What does it mean, and what would I do?

A merge conflict means Git cannot automatically combine changes... because two branches changed the same lines or made incompatible edits. I would inspect the affected files and conflict markers, understand both changes, decide how they should be combined, remove the markers, run the relevant tests, then stage and commit the resolution. If I am unsure which behaviour is correct, I would ask the relevant teammate rather than guessing.

### Scenario 4: I have not been assigned a development task yet. What should I do this week?

I would not wait passively. I would set up and run the project, study its structure and documentation, learn the tools and workflow being used, review existing components and APIs, and look for small issues or documentation improvements I could contribute to. I would also ask the team where help is most useful once I have enough context.
