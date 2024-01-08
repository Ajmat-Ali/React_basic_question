1. What is React?

   React is a JavaScript library used for building user interfaces, particularly for creating interactive and dynamic web applications. It helps developers efficiently update and render components in response to data changes, making it easier to manage and organize the UI of a web application.

2. Who made React?

   React was created by Jordan Walke, a software engineer at Facebook.

3. What is Babel?

Babel is a JavaScript compiler. In the context of web development, Babel is primarily used to transform ECMAScript 2015+ (ES6+) code into a backward-compatible version of JavaScript that can run in older browsers or environments. It allows developers to use the latest JavaScript features and syntax, even if the target environment doesn't support them natively.

4. How does Babel convert html code in React into valid code?

Babel doesn't directly handle HTML code; its main job is to transform JavaScript code. However, when working with React, which uses a syntax called JSX for defining components, Babel comes into play.
JSX looks a lot like HTML, but browsers don't understand it. Babel translates JSX into regular JavaScript so that browsers can run it.

Example:- it converts JSX expressions like:
const element = <h1>Hello, React!</h1>;

Into standard JavaScript code like:
const element = React.createElement('h1', null, 'Hello, React!');

5.  What is ReactDOM used for? Write an example?
    ReactDOM is a library in React that helps you take your React components and render them into the HTML DOM (Document Object Model). In simpler terms, it's the part of React that makes your components show up on a webpage.

    Here's a basic example:

                 Let's say you have a React component called MyComponent:
                 // MyComponent.jsx

                 import React from 'react';

                 const MyComponent = () => {
                 return <h1>Hello, React!</h1>;
                 };

                 export default MyComponent;

Now, you want to show this component on a webpage. This is where ReactDOM comes in. You use ReactDOM's render function to place your React component into the actual HTML DOM:
// index.js

                import React from 'react';
                import ReactDOM from 'react-dom';
                import MyComponent from './MyComponent';

                ReactDOM.render(<MyComponent />, document.getElementById('root'));

6.  What are the packages that you need to import for react to work with?
    React is the core library for building user interfaces using components.
    a) React:
    React is the core library for building user interfaces using components.
    Ex:- import React from 'react';
    b) ReactDOM:
    ReactDOM is used for rendering React components into the DOM.
    Ex:- import ReactDOM from 'react-dom';
    c) Babel:
    Babel is a JavaScript compiler that allows you to use the latest JavaScript features, especially when writing React code in JSX.
    Ex:- // This import may vary based on your Babel configuration
    import 'babel-polyfill';

7.  How do you add react to a web application?
    Step 1: Add a DOM Container to the HTML
    First, open the HTML page you want to edit. Add an empty <div> tag to mark the spot where you want to display something with React. For example:

             Ex:-   <!-- ... existing HTML ... -->

                <div id="like_button_container"></div>

                <!-- ... existing HTML ... -->

    Step 2: Add the Script Tags
    Next, add three <script> tags to the HTML page right before the closing </body> tag:

            Ex:-  <!-- ... other HTML ... -->

                <!-- Load React. -->
                <!-- Note: when deploying, replace "development.js" with "production.min.js". -->
                <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
                <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>

                <!-- Load our React component. -->
                <script src="like_button.js"></script>

                </body>

    Step 3: Create a React Component
    Create a file called like_button.js next to your HTML page.  
     // ... the starter code you pasted ...

                const domContainer = document.querySelector('#like_button_container');
                const root = ReactDOM.createRoot(domContainer);
                root.render(e(LikeButton));

8.  What is React.createElement?
    `React.createElement` is a function provided by React that is used to create React elements in your JavaScript code. It is an essential part of how JSX (JavaScript XML) syntax is translated into regular JavaScript code

9.  What are the three properties that createElement accept?
    `React.createElement` accepts three main properties:
        1) Type:
             The first argument to React.createElement is the type of the React element you want to create.
                Ex:- `React.createElement('h1', /* ... */);` // HTML element
        2) Props:
            The second argument is an optional object that represents the properties (or props) you want to assign to the element.
             Ex:-  React.createElement('h1', { className: 'title' }, 'Hello, React!');
        3)Children:
            The remaining arguments represent the children of the element, representing its content. Children can be strings, other React elements, or an array of these.
            Ex:-  React.createElement('div', null, 'This is a div element');

        `Final Example` :- React.createElement(type, props, ...children);

10. What is the meaning of render and root?
    1)Render:
    In React, "render" refers to the process of converting React components into DOM elements and displaying them on the screen. The ReactDOM.render() function is a key part of this process. It takes a React element (or a tree of React elements) and mounts it into the specified DOM node.
    Ex:- ReactDOM.render(<App />, document.getElementById('root'));

    2)Root:
    The term "root" in React commonly refers to the root DOM element where your React application is mounted. It's the top-level container in your HTML file where your React components will be rendered.

        Ex:-  <div id="root"></div>
