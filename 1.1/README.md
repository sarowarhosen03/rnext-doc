# Module 1.1

## **What is React?**

React is a javascript UI/User Interface Library.

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

## What is Bable?

Bable is a Javascript Transpiler. Its **Primary Role** is to translate modern Javascript code to the old version of javascript.

## What is JSX

JSX's full form is 'JavaScript XML'. It's XML like an extension of Javascript for building UI components. It was created on Facebook by the React team for Reactjs.

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
