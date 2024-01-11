# 1.6 - Basics of JSX: React's Markup - Writing Markup with JSX

\***\*What is JSX:\*\***

JSX stands for **JavaScript XML**. It is a syntax extension for JavaScript that lets you write HTML-like markup inside a JavaScript file. Although there are other ways to write components, most React developers prefer the conciseness of JSX, and most codebases use it. For further knowledge you can check [JSX section](https://react.dev/learn/writing-markup-with-jsx) from React documentation.

# Why we need it ?

We can write react code with or without jsx. But that will be a time consuming process. In react we can create element with 'createElment' method like below.

createElement method takes 3 arguments

<ol>
    <li>Type - specify which element we want ex:  'h1', 'p', 'span' etc. </li>
    <li>Props - if we want to provide any props, If not then we will provide null</li>
    <li>childen - whether we want to pass one element into another (nested eleement's) </li>
</ol>


```jsx
Import React from 'react';

const element = React.createElement('h1', null, 'hello world');
```

in the above code we are creating a h1 element with the text 'hello world' in it as it's innerText. Now what if we want a span tag inside our h1 tag. Let's see.

```jsx
Import React from 'react';

const element = React.createElement('h1', null, React.createElement('span', null, 'Hello span'));
```

we have to call another createElement method in 3rd params and it will create nested elements that will look like this in HTML.

- in HTML -

```html
<h1>
   <span>Hello span</span>
</h1>
```

as you can assume if we want to make our whole markup like this, how messy our codebase will look like and this is the reaseon why JSX is here. Now let see how will the above code look like in jsx.

- in JSX -

```jsx
<h1>
   <span>Hello span</span>
</h1>
```

your are thinking this is HTML, no it's not HTML. It look like HTML but has more superpower in it. It can take any dynamic value and javaScript expresssion in {}. It has many build in HTML elements. It is really easy to work with JSX.

# The Rules of JSX

<ol>
    <li>Return a single root element</li>
    <li>Close all the tags</li>
    <li>camelCase all most of the things!</li>
</ol>

**For historical reasons, aria-_ and data-_ attributes are written as in HTML with dashes.**

**Explanation of the Rules of JSX**

# Why do we have to write the attributes in camelCase ?

As I have said earlier this not HTML. So to differenciat JSX from HTML, we have to write some known attribute in camelCase like this. And there is some javaScript reserve keyword that can't be used like the 'class', we have to write 'className' in JSX. Below giving some sample code to understand it bit more

html

```html
<button type="button" class="btn btn-large" onclick="printFive()">Click Me</button>
```

in JSX it will be

```jsx
<button type="button" className="btn btn-large" onClick={printFive}>
   Click Me
</button>
```

see this list of attributes supported by div element. [See more](https://react.dev/reference/react-dom/components/common)

# Why have we have to close all tags ?

In HTML there are many self closing tags like `<img>`, `<br>` , `<area>` and much more, But in JSX every tag should be closed

# Why we have to return a single root element, why can't we return multiple element from JSX ?

To understand that you have to know what JSX return, JSX transpile to javaScript object {}. In this object JSX has all the information of element that it represents. With the help of this object React creates dom nodes. Print the below component in console and see what it returns.

```jsx

export default function List () {
    return <li>hello</li>;
}

```
Now you know jSX return object, But why do we have to wrap mulltiple element in a div or something (root element) in JSX, that's bcz function can't return multiple object like below, it's a SyntaxError in javaScript.

```jsx
export default function App () {
    return {}{}.
}
```

Think of it like this: either we have to wrap it with a single object like `{{}{}}` (hence the `<div>` tag), or we have to use a fragment (<>...</>) and write inside of this. Internally, it will return an array of multiple objects like `[{}{}]`. Here, the objects are the JSX elements as mentioned earlier.