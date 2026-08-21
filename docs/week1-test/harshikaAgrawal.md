# Week 1 Test
**NAME:** Harshika Agrawal
**Team:** development team (desktop)

## What I learned this week
- **Git/GitHub:**
- **JavaScript:**

## One thing I am still confused about
-the exact contents of the group that is what exactly this app will contain.

## One thing I think I can contribute to the project
-
--------------------------------------------------------------------------------------------------------
## PART 2 — Git/GitHub Questions

1. What is the difference between `git` and GitHub?
- Git is used for tracking and saving files locally whereas github is used to store the files online and also share it.
i can write and edit my code in vscode then save it and push it on github using git commands such as 'git add .', 'git push origin main' . Git tracks the changes I make to that code. GitHub is where I save or host my repos online, connect with other people, and collaborate — I can go through or contribute to others' projects, and others can do the same with mine (usually via forking + Pull Requests, not direct editing, unless they've been given access).

2. What is a branch and why are we using separate branches instead of working directly on `main`?
- Branch option is used to edit the code files by cloning the main repo. it allows us to edit the branch without changing the main repo. it is used for creating different changes to the code at the same time. if a group of people are working separately on the same project they can create different branches, see the difference in each branch and even merge it if needed.

3. What does this do?   git pull origin main
it is used to save the changes from github to your computer.it is the opposite of git push.

4. What is the difference between:
   - `git add .`-- stage the changes
   - `git commit` --  to save the changes locally
   - `git push` -- upload the changes to github

5. What is a Pull Request?
it is a format request asking someone to merge your changes to their branch.

6. Why shouldn't you directly push to `main` in our project?
pushing to main directly should be avoided as if the changes you made causes some error it may cause trouble to others woking on the same thing. also they will not be able to work on the original code anymore.

7. What would you do if you start working on a task and someone else has already pushed changes to `main`?
I would switch to the main, pull the latest changes, then switch back to my branch and merge it with the main. this will keep my branch up to date before i may start editing it.

8. What makes a good commit message? Give two examples.
a good commit message may include the actual task of the code or the changes made to make it convenienet for you or others later to know what is actually done in the task.
**Example--** "answers to test1" , "updating the design of the website through css" etc.

--------------------------------------------------------------------------------------------------------

## PART 3 — JavaScript Basics

### 1. Variables

**What is the difference between:**
- `let` - can't redeclare but update. If we use it in our code, we have to declare it only once but we can add changes to it through the code whenever needed.

- `const` - can't redeclare or update. once we declare a variable and give some value to it we can't further change its value.

- `var` - redeclared and updated. We have to declare the variable everytime we are using it . We can also change the value each time.

**Which ones would you normally use in our project?**
I would use let in  my code as it is the mot appropriate one for me.

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
The 1st one is the direct way of writing the function meanwhile the 2nd way is the compact way of writing a function(Arrow function). the 1st one is the oid and explicit way of writing a function whereas the arrow function is the newer and shorter way of writing the function.

### 3. Arrays

What will this produce?
```javascript
const numbers = [1, 2, 3, 4];
const result = numbers.map(n => n * 2);
```


### 4. map, filter, find

Explain what these do:
- `map()`
- `filter()`
- `find()`

Give one simple example of each.

### 5. Objects

What does this represent?

```javascript
const child = {
    name: "Alex",
    age: 8,
    interests: ["drawing", "music"]
};
```

How would you access the child's name?

### 6. Destructuring

What does this do?

```javascript
const { name, age } = child;
```

### 7. Async/Await

What is the purpose of:
- `async`
- `await`

Why would we need them when communicating with a backend/API?

### 8. API

Suppose the backend gives us: `GET /api/children`

What do you think this endpoint is used for?

--------------------------------------------------------------------------------------------------------

## PART 4 — React / Expo Basics

### 1. What is React?

Explain in your own words what React is used for.

### 2. What is a component?

What do you think this means?

```javascript
function Welcome() {
    return <Text>Hello!</Text>;
}
```

### 3. State

What is `useState()` used for?

Give one example where we might use state in Neuronest.

### 4. Props

What are props in React?

### 5. Expo

What is Expo and why are we using it?

### 6. Running the project

What command would you use to start an Expo development server?

What is the purpose of: `npx expo start`

### 7. Platform

Why might we use Expo/React Native instead of building completely separate Android and iOS applications?

--------------------------------------------------------------------------------------------------------

## PART 5 — Team Workflow

Answer these based on our project's workflow, not just generic Git knowledge.

### Scenario 1

You are assigned: "Implement the login screen."

What would you do before starting?

### Scenario 2

You are working on your branch and someone else has merged changes into `main`.

What should you do before opening your PR?

### Scenario 3

You get a merge conflict.

What does that mean? What would you do?


### Scenario 4

You haven't been assigned a development task yet.

What should you be doing during this week?
