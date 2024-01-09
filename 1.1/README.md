# Module 1.1

## **What is React?**

React is a javascript UI/User Interface Library.

## Why React ?

ReactJS is a UI library that helps us build dynamic and efficient user interfaces with reusable code. It simplifies DOM manipulation and enhances the responsiveness of web apps. The UI automatically reacts to data changes, eliminating the need to manually specify how and when updates should occur.

## Spacial Feature?

-   Declarative. [Declarative means we describe what we want, not how to do it.]
-   State Management
-   Component-Based Architecture/Reusable Code
-   VDOM
-   JSX

## Transpiler, Bable and JSX.

### What is Transpiler?

Transpiler is a tool that take code written in one language and convert it to another language.

## What is Bable?

Bable is a Javascript Transpiler. It's **Primary Role** is to translate modern Javascript code to old version of javascript.

## What is JSX

JSX's full form is 'JavaScript XML'. It's XML like extention of Javascript for building UI component. It was creeated at Facebook by React team for Reactjs.

## How JSX, Bable and React work together?

As Browser do not understand JSX syntax, JSX syntax are parsed by Bable. Bable creats JS code that browser can understand. For Ex:

This is a JSX code:

```JSX
const WelcomeButton = () => (
  <button onClick={() => alert('Hello!')}>Click me!</button>
);
```

After it was Transpiled by Bable, The output is:

```JS
const WelcomeButton = () => (
  React.createElement("button", { onClick: () => alert('Hello!') }, "Click me!")
);
```

Now the output is a pure JS code which browser understand.
