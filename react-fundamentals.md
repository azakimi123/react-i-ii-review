### Remember

Answer these on your own, then compare answers as a group

1.  What is React?
    - React is a javascript library composed of different methods
    - Focuses on making UI elements and has a virtual DOM
    - A collection of dependencies for building a React App
    - component based architecture 
    - unidirectional data flow


2.  What is create-react-app?
    - It is a tool that gives you different configurations that helps you to create an React app with little set up needed. 
    - a tool for puting together a React app in one go
    - a development environment with auto-refresh (npm start)

3.  What is Component Based Architecture?
    - A way to break down a larger project into smaller "components" or pieces of code to help debug and manage.
    - modular concept to another level
    - easily create scalable apps
    - self-sustaining individual blocks of code

4.  What is JSX?
    - It is a mix of HTML/JS used in React
    - Syntax uses to describe user interface

5.  What is the virtual DOM?
    - It is similar to the DOM, but things are kept in memory and can be run      faster.  Updates just what is updated instead of going through the whole document
    - A memory representation of the DOM that stays in sync with the real DOM
    - A "mock DOM" that keeps a copy of the actual DOM
    - it increases the performance

6.  What is unidirectional (one-way) data flow?
    - Data can only passed one way, parents to children
    - We can get around this by passing info up through events

### Understand

Discuss these questions in pairs if you have a 4-person group

7.  Summarize what happens when you run `create-react-app my-app`
    - It creates a react app by setting up different folders and files with node modules to create the app. 
    - names the folder 'my-app'
    - folder includes our boiler plate
    - It creates the git repo for the app and the package.json necessary to keep track of dependencies

8.  Explain what this code does:

```jsx
import React from "react";

const Mentor = props => (
  <div className="mentor-container">
  // ternary
    <h1 className={props.title === "Lead Mentor" ? "lead" : ""}>Tim Biles</h1>
    <ul>
      <li>Fort Worth, TX</li>
      <li>My email address is timbilestimbiles@gmail.com</li>
    </ul>
  </div>
);

export default Mentor;
```

9.  Explain how data is passed from a parent component to a child component.
    - props
### Apply

Try these on your own, but work together if you start to get stuck.

10.  Use `create-react-app` to create a new React application called `student-directory`

11.  Use the code from `Mentor` above to create a new functional, stateless component called `User` with a list of friends. Hard code the list of friends, do not use state or props.

### Analyze, Evaluate, Create

Discuss these questions as a group

12. What are the benefits and drawbacks of using a tool like create-react-app?
    - Benefits
        - Can throw together a React app quickly
        - Don't need to install individual pieces required in a React app
        - Most of the setup (think, config files, etc) already done for us
    - Drawbacks
        - It could potentiall install something that you don't need(bigger app size)

13. Compare and contrast JSX with other templating options, such as those used in Angular or Vue

14. Compare and contrast one-way data flow with two-way data binding.
    - One-way = unidirectional
    - Two-way = bidirectional 
