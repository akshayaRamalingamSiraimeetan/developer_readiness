# Week 1 Developer Readiness Assessment

Complete all sections below. Use this repository for the practical Git tasks.

---

## PART 1 — Git & GitHub Practical Task

Use this repository for the following tasks.

### 1. Clone the repository

Clone this repository to your local machine.

**Be able to explain:**
- What `git clone` does
- Difference between a local repository and the GitHub repository

### 2. Create a branch

Create a branch using the format: `yourname-week1-test`

**DO NOT** make any changes directly on `main`.

### 3. Make a small change

Create the file: `docs/week1-test/yourname.md`

Inside it, put:

```markdown
# Week 1 Test

**Name:** [Your name]
**Team:** [Your team/role]

## What I learned this week

- **Git/GitHub:** 
- **JavaScript:** 
- **Expo:** 
- **Neuronest:** 

## One thing I am still confused about

- 

## One thing I think I can contribute to the project

- 
```

### 4. Commit your changes

Use a meaningful commit message.

**Good example:** `Add week 1 developer assessment`

**Bad examples:** `done`, `changes`, `update`, `final`, `test`, `asdf`

### 5. Push your branch

Push your branch to GitHub.

### 6. Create a Pull Request

Create a Pull Request: `yourname-week1-test → main`

The PR description should contain:

```markdown
## What I did
- 

## What I learned
- 

## Anything I am still unclear about
- 
```

**DO NOT** merge your own PR.

---

## PART 2 — Git/GitHub Questions

1. What is the difference between `git` and GitHub?

2. What is a branch and why are we using separate branches instead of working directly on `main`?

3. What does this do?
   ```bash
   git pull origin main
   ```

4. What is the difference between:
   - `git add .`
   - `git commit`
   - `git push`

5. What is a Pull Request?

6. Why shouldn't you directly push to `main` in our project?

7. What would you do if you start working on a task and someone else has already pushed changes to `main`?

8. What makes a good commit message? Give two examples.

---

## PART 3 — JavaScript Basics

### 1. Variables

What is the difference between:
- `let`
- `const`
- `var`

Which ones would you normally use in our project?

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

---

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

---

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

You are confused because the documentation says one technology, but you remember us discussing another technology in the meeting.

What should you do?

### Scenario 5

You haven't been assigned a development task yet.

What should you be doing during this week?

**Note:** The expected behavior is NOT "Wait until Akshaya gives me a task."

You should be:
- Exploring the assigned technology stack
- Understanding the documentation
- Setting up your environment
- Learning Git/GitHub
- Running the project if available
- Understanding the project structure
- Preparing yourself for development
- Documenting questions and blockers

---

## PART 6 — Practical Project Run

**If the Neuronest development environment has already been provided separately**, follow the team's instructions to run the actual application.

**Do NOT** copy the actual Neuronest source code into this assessment repository.

Tasks:
1. Clone the actual Neuronest repository (separate from this one)
2. Create your branch
3. Install dependencies
4. Run the Expo project
5. Open it on an emulator or physical device
6. Take a screenshot of the running application
7. Add the screenshot to your Pull Request in this assessment repository

**Note:** Actually running software is more useful than simply asking whether someone "knows Expo."

---

## Completion

Once you have completed all sections:

1. Commit your answers to your branch
2. Push your branch to GitHub
3. Open a Pull Request
4. Request a review
5. **DO NOT** merge your own PR

Remember: This assessment helps identify learning gaps. Not knowing something is completely normal and expected!