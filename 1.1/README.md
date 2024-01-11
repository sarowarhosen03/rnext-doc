# Module 1.1

## **What is React?**

React is a javascript UI/User Interface Library. **The user interface involves two main processes:**

1. (Creating the DOM) The creation of the DOM (Document Object Model) refers to the browser's rendering of the HTML file. HTML supports JavaScript in creating the DOM, which is preferred over creating it using JavaScript since the latter can be quite complicated[.](http://2.to)

2. (User interaction) After creating the DOM, JavaScript manipulates it to create user interactions.

In React, user interactions are handled by React, while ReactDOM renders the DOM. Before creating a DOM, a virtual DOM is created, which is one of React's main advantages.

- **The difference between a library and a framework:**
    - **Library:** This is the focus for building any particular thing. For example, React for web and native user interfaces.
    - ****Framework:**** This is the complete package for any project. The framework for JavaScript, for example, is shown next.

- **React's invention:**
    - Jordan Walke created it. He was inspired by the PHP framework based on the XHP-JS component, which was used in the Facebook newsfeed in 2011.

## Why React?

ReactJS is a UI library that helps us build dynamic and efficient user interfaces with reusable code. It simplifies DOM manipulation and enhances the responsiveness of web apps. The UI automatically reacts to data changes, eliminating the need to manually specify how and when updates should occur.

## Spacial Feature?

-   Declarative. [Declarative means we describe what we want, not how to do it.]
-   State Management
-   Component-Based Architecture/Reusable Code
-   VDOM
-   JSX

## Transpiler, Bable and JSX.

### What is Transpiler?

Transpiler is a tool that takes code written in one language and converts it to another language.

- **Compiler VS Transpiler**
    - **Compiler:** Compilers are used to convert higher levels of code (human-understandable) to a binary file (machine-understandable code). **Examples** of compiled languages are C, C++, and Java, which, after compiling, generate bytecodes, or assembly-level languages, which are closer to binary files.
      
    - ************************Transpiler:************************ Transpiling can be referred to as a source-to-source compiler, which translates one higher-level language to another higher-level language. **For example,** Typescript is a higher-level language that, after transpiling is converted to JavaScript, which is also another higher-level language

## What is Bable?

Babel is a JavaScript compiler. Also, this is a transpiler. Babel can convert JavaScript ES6 syntax to ES5 syntax to ensure compatibility with all older browsers. For this, we use Bable.

## What is JSX

The full form of JSX is 'JavaScript XML'. It is an extension of JavaScript for creating UI components. JSX allows you to write HTML-like code in JavaScript files, making working with UI components easier. It was created on Facebook by the React team for Reactjs.

## How do JSX, Bable and React work together?

As Browser does not understand JSX syntax, JSX syntax is parsed by Bable. Bable creates JS code that the browser can understand. For Ex:

This is a JSX code:

```JSX
const WelcomeButton = () => (
  <button onClick={() => alert('Hello!')}>Click me!</button>
);
```

After it was transpiled by Bable, The output is:

```JS
const WelcomeButton = () => (
  React.createElement("button", { onClick: () => alert('Hello!') }, "Click me!")
);
```

Now the output is a pure JS code which the browser understands.
