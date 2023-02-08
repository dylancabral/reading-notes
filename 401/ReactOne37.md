# React

React is a JavaScript library for building user interfaces. It was developed and is maintained by Facebook. React allows developers to build and manage the state of complex UI components using a concept called "virtual DOM". React updates the actual DOM efficiently and only when necessary, improving the overall performance of the application. React also provides a way to easily reuse UI components, making it easier to maintain and scale large applications. With React, developers can create fast, dynamic, and interactive user interfaces for web and mobile applications.


## Jsx

- JSX is a syntax extension for JavaScript that allows writing HTML-like code within JavaScript.
- React uses JSX to define components and their elements.
- The code written in JSX gets transpiled to JavaScript code that can run in the browser.
- JSX elements can have JavaScript expressions within curly braces {}.
- JSX elements must have a single parent element and can't be returned from a function as separate elements.

## Rendering elements

- React elements are objects that represent the component's desired output.
- React elements are created using the React.createElement() method or the JSX syntax.
- React elements are the building blocks of React components.
- React elements are immutable and cannot be changed once they are created.
- To update the component, a new React element must be created and passed to ReactDOM.render().
- ReactDOM.render() is used to render React elements to the DOM.
- The first argument to ReactDOM.render() is the React element, and the second argument is the DOM node where the element should be rendered.

## Next Js

- Next.js is a React-based framework for building server-rendered or statically exported web applications.
- Next.js provides a simple way to create a new Next.js project using the create-next-app command-line tool.
- The create-next-app tool sets up a new Next.js project with a basic file structure and dependencies.
- The created Next.js project includes a pages directory that contains the application's pages and routes.
- Next.js uses automatic code splitting to optimize the performance of the application by only loading the necessary JavaScript for each page.
- Next.js also provides features such as automatic CSS processing, optimized asset loading, and built-in optimization for search engine optimization (SEO).
- To start the development server, run the npm run dev command in the project's root directory.
- To build the application for production, run the npm run build command and then the npm start command to start the production server.

`create-next-app`: Command-line tool used to create a new Next.js project.
`ReactDOM.render()`: Renders React elements to the DOM.
`npm run dev`: Starts the development server for the Next.js project.
`npm run build`: Builds the Next.js project for production.
`npm start`: Starts the production server for the Next.js project.

## Things I want to know more about 

all of it, I want to know more about tailwind it seems very cool

## Resources

[React - JSX](https://reactjs.org/docs/introducing-jsx.html)

[React - Rendering Elements](https://reactjs.org/docs/rendering-elements.html)

[React - Components & Props](https://reactjs.org/docs/components-and-props.html)

[React - State & Lifecycle](https://reactjs.org/docs/state-and-lifecycle.html)

[React - Handling Events](https://reactjs.org/docs/handling-events.html)

[Utility First CSS](https://tailwindcss.com/docs/utility-first)

[Utility First CSS](https://www.youtube.com/watch?v=6zIuAyLZPH0)

[Tailwind in 15 minutes](https://www.youtube.com/watch?v=6zIuAyLZPH0)

[Learn Next.js](https://nextjs.org/learn/basics/create-nextjs-app)

[Why to use Next.js](https://www.youtube.com/watch?v=rtgbaKBhdkk)