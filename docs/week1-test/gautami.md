# Week 1 Test

**Name:** Gauatmi Yeshwant Deshpande
**Team:** Development Team

## What I learned this week

- **Git/GitHub:**learned how branches, commit,push and pull work
- **JavaScript:**learned basics of JS

## One thing I am still confused about

-

## One thing I think I can contribute to the project

-

PART 2 — Git/GitHub Questions
What is the difference between git and GitHub?
git is version control system whih runs on our own computer.
github is clued based platform to collaborate w other developers.

What is a branch and why are we using separate branches instead of working directly on main?
branch is indepndent line of development in git repo.
helps each devloper to work on their own branch i.e. allows multiple developers to work simultaneoulsy.

What does this do?git pull origin main
get the lastest chnges from the main branch on github repo and combine them into current local branch.

What is the difference between:git add .   git commit     git push
git add . moves all chnges for next commit
git commit save the changes as a version in local git history
git push uploads commit from local repo to github

What is a Pull Request?
a request to merge changes from one branch to another

Why shouldn't you directly push to main in our project?
due to conflicting changes

What would you do if you start working on a task and someone else has already pushed changes to main?
we should synchronize our branch w the latest main and use git fetch origin to get the latest information from github

What makes a good commit message? Give two examples.
a good commit message should be concise and focus on what we have updated.

PART 3 — JavaScript Basics
1. Variables
What is the difference between:let,const,var.
Which ones would you normally use in our project?
let: when the variables value needs to be chnaged
const: when variables value shouldnt be reassigned
var:used to declare variables that are either globally or function scoped

2. Functions
What is the difference between:
function add(a, b) {
  return a + b;
}
this is reular function declaration
and:
const add = (a, b) => {
  return a + b;
};
this is an arrow function which stores the function inside a const variable


3. Arrays
What will this produce?
const numbers = [1, 2, 3, 4];
const result = numbers.map((n) => n * 2);
[2,4,6,8]

4. map, filter, find
Explain what these do:

map(): transforms every element
const num=[1,2,3]
const doub=num.map((n)=>n*2);
filter():keeps elements that satisfy a conditon
const num=[1,2,3,4]
const eve=num.filter((n)=>n%2==0);
find():return the first element satisfying a condition
const num=[1,2,3]
const res=num.find((n)=>n>2);
Give one simple example of each.

5. Objects
What does this represent?
const child = {
  name: "Alex",
  age: 8,
  interests: ["drawing", "music"],
};
How would you access the child's name?
child.name

6. Destructuring
What does this do?
const { name, age } = child;
allows to extract properties from an object and bind them to distinct variables 

7. Async/Await
What is the purpose of:
async
await
Why would we need them when communicating with a backend/API?

8. API
Suppose the backend gives us: GET /api/children

What do you think this endpoint is used for?

PART 4 — React / Expo Basics
1. What is React?
Explain in your own words what React is used for.

2. What is a component?
What do you think this means?

function Welcome() {
  return <Text>Hello!</Text>;
}
3. State
What is useState() used for?

Give one example where we might use state in Neuronest.

4. Props
What are props in React?

5. Expo
What is Expo and why are we using it?

6. Running the project
What command would you use to start an Expo development server?

What is the purpose of: npx expo start

7. Platform
Why might we use Expo/React Native instead of building completely separate Android and iOS applications?

PART 5 — Team Workflow
Answer these based on our project's workflow, not just generic Git knowledge.

Scenario 1
You are assigned: "Implement the login screen."

What would you do before starting?

Scenario 2
You are working on your branch and someone else has merged changes into main.

What should you do before opening your PR?

Scenario 3
You get a merge conflict.

What does that mean? What would you do?

Scenario 4
You haven't been assigned a development task yet.

What should you be doing during this week?

Note: The expected behavior is NOT "Wait until you are given a task."