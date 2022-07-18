- [What is React?](#what-is-react)
- [What are the advantages of using React?]
- [What are the limitations of React?]
- [What is JSX?](#what-is-jsx)
- [What are the differences between functional and class components?]

### What is React?
React is a front-end and open-source Javascript library which is useful in developing user interfaces specifically for Single Page Applications. It is helpful in building complex and reusable UI components of mobile and web applications as it follows the component-based approach.
The important features of React are
- It supports server-side rendering.
- It makes use of virtual DOM rather than real DOM as real DOM manipulation are expensive.
- It follows unidirectional data binding or data flow.
- It uses reusable or composable UI components for developing the view.

### What are the advantages of using React?
- Virtual DOM: React uses Virtual DOM to render the view. As the name suggests, virtual DOM is a virtual representation of the real DOM. Each time the data changes in a react app, a new virtual DOM gets created. Creating a virtual DOM is much faster than rendering the UI inside the browser. Therefore, with the use of virtual DOM, the efficiency of the app improves.
- Reusable components: React uses component-based architecture of developing applications. Components are independent and reusable bits of code. These components can be shared across various applications having similar functionality. The re-use of components increases the pace of development.
- SEO friendly: React allows developers to develop engaging user interfaces that can be easily navigated in various search engines. It also supports server-side rendering, which boots the SEO of an app.
- Huge ecosystem of libraries: React provides you with the freedom to choose the tools, libraries, and architecture for developing an application based on your requirement.
- Gentle learning curve: React has a gentle learning curve when compared to frameworks like Angular. Anyone with little knowledge of Javascript can start building web applications using React.

### What are the limitations of React?
- React is not a full-blown framework as it is only a library.
- The components of React are numerous and will take time to fully grasp the benefits of all.
- It might be difficult for beginner programmers to understand React.
- Coding might become complex as it will make use of inline template and JSX.

### What is JSX?
JSX is a syntax extension to Javascript which provides a way to structure component rendering. It allows us to write HTML inside Javascript and place them in the DOM. React doesn’t require using JSX.
- Embedding Expression in JSX
You can put any valid Javascript expression inside the curly braces in JSX.
Examples:
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;
- JSX is an Expression Too
- Specifying Attributes with JSX
- JSX prevents injection attacks
By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application.
- JSX Represents Objects
Babel compiles JSX down to React.createElement() calls.

### What are the differences between functional and class components?
Before the introduction of Hook in React, functional components were called stateless components and were behind class components on a feature basis. After the introduction of Hooks, functional components are equivalent to class components. 
- Declaration
Functional components are nothing but Javascript functions and therefore can be declared using an arrow function or the function keyword. Class components, on the other hand, are declared using ES6 class.
- Handling props
In functional component, the handling of props is pretty straightforward. Any prop provided as an argument to a functional component can be directly used inside HTML elements.
In case of class component this keyword is used.
- Handling state
Functional components use React hooks to handle state. It uses the useState hook to set the state of a variable inside the component. We cannot use React Hooks inside class components, therefore state handling is done very differently in a class component. 
We use this.state to read the state.
For updating the state, we need to first bind the function to this. Only then, we will be able to use the setState function which is used to update the state.
Explain React state and props
The props in React are the input to a component of React. Every React component accepts a single object argument called props. These props can be passed to a component using HTML attributes and the component accepts these props as an argument.
Every component has a built-in state object, which contains all the property values that belong to that component. In other words, the state object controls the behavior of a component. Any change in the property values of the state object leads to the re-rendering of the component.
State object is not available in functional components but, we can use React Hooks to add state to a functional component.
Props are immutable. Has better performance than state. Can be passed to child compoents.
State object is owned by the component, locally scoped and mutable. Has setState() method to modify properties. Changes to state can be asynchronous. Can be only passed as props.
What is the Virtual DOM? How does react use the Virtual DOM to render the UI?
