# 1.4 - Basics of React Components: Your first component

\***\*Defining a component:\*\***

Traditionally, when creating web pages, web developers marked up their content and then added interaction by sprinkling on some JavaScript. This worked great when interaction was a nice-to-have on the web. Now it is expected for many sites and all apps. React puts interactivity first while still using the same technology: **a React component is a JavaScript function that you can _sprinkle with markup_.** Here’s what that looks like (you can edit the example below):

```jsx
export default function Profile() {
  return <img src="https://i.imgur.com/MK3eW3Am.jpg" alt="Katherine Johnson" />;
}
```

## **How to build a component**

### **Step 1: Export the component**

The `export default` prefix is a [standard JavaScript syntax](https://developer.mozilla.org/docs/web/javascript/reference/statements/export) (not specific to React). It lets you mark the main function in a file so that you can later import it from other files. (More on importing in [Importing and Exporting Components](https://react.dev/learn/importing-and-exporting-components)!)

### \***\*Step 2: Define the function\*\***

With `function Profile() { }` you define a JavaScript function with the name `Profile`.

### \***\*Step 3: Add markup.\*\***

The component returns an `<img />` tag with `src` and `alt` attributes. `<img />` is written like HTML, but it is actually JavaScript under the hood! This syntax is called [JSX](https://react.dev/learn/writing-markup-with-jsx), and it lets you embed markup inside JavaScript.

Return statements can be written all on one line, as in this component:

```jsx
return <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />;
```

But if your markup isn’t all on the same line as the `return` keyword, you must wrap it in a pair of parentheses:

```jsx
return (
  <div>
    <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />
  </div>
);
```

### \***\*Using a component\*\***

Now that you’ve defined your `Profile` component, you can nest it inside other components. For example, you can export a `Gallery` component that uses multiple `Profile` components:

```jsx
function Profile() {
  return <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />;
}

export default function Gallery() {
  return (
    <section>
      <h1>Amazing scientists</h1>
      <Profile />
      <Profile />
      <Profile />
    </section>
  );
}
```
