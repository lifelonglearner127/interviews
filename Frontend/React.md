- [What is React?](#what-is-react)
- [Advantages of React?](#advantages-of-react)
- [Limitations of React?](#limitations-of-react)
- [What is useState() in React](#what-is-usestate-in-react)
- [What are keys in React?](#what-are-keys-in-react)
- [What is JSX?](#what-is-jsx)
- [Differences between functional and class components?](#differences-between-functional-and-class-components)
- [About Virtual DOM](#about-virtual-dom)
- [Differences between controlled and uncontrolled components](#about-virtual-dom)
- [Explain React state and props](#explain-react-state-and-props)
- [Explain about types of side effects in React Component](#explain-about-types-of-side-effects-in-react-component)
- [What is prop drilling in React?](#what-is-prop-drilling-in-react)
- [What are error boundaries?](#what-are-error-boundaries)
- [Explain React Hooks?](#explain-react-hooks)
- [What is the use of useEffect React Hooks?](#what-is-the-use-of-useeffect-react-hooks)
- [Why do React Hooks make use of refs?](#why-do-react-hooks-make-use-of-refs)
- [What are Custom Hooks](#what-are-custom-hooks)
- [Explain Strict Mode in React](#explain-strict-mode-in-react)
- [How to prevent re-renders in React?](#how-to-prevent-re-renders-in-react)
- [What are the different ways to style a React component?](#what-are-the-different-ways-to-style-a-react-component)
- [Techniques to optimize React app performance](#techniques-to-optimize-react-app-performance)
- [How to pass data between react components](#how-to-pass-data-between-react-componentss)
- [What are Higher Order Components?](#what-are-higher-order-components)
- [What are the different phases of the component lifecycle?](#what-are-the-different-phases-of-the-component-lifecycle)
- [What are the lifecycle methods of React?](#what-are-the-lifecycle-methods-of-react)
- [Does React Hook work with static typing?](#does-react-hook-work-with-static-typing)
- [Explain about types of Hooks in React.](#explain-about-types-of-hooks-in-react)
- [Differentiate React Hooks vs Classes.](#differentiate-react-hooks-vs-classes)
- [How does the performance of using Hooks will differ in comparison with the classes](#how-does-the-performance-of-using-hooks-will-differ-in-comparison-with-the-classes)
- [Do Hooks cover all the functionalities provided by the classes?](#do-hooks-cover-all-the-functionalities-provided-by-the-classes)
- [What is React Router?](#what-is-react-router)
- [Can React Hook replaces Redux?](#can-react-hook-replaces-redux)

### What is React?
React is a front-end and open-source Javascript library which is useful in developing user interfaces specifically for Single Page Applications. It is helpful in building complex and reusable UI components of mobile and web applications as it follows the component-based approach.
The important features of React are
- It supports server-side rendering.
- It makes use of virtual DOM rather than real DOM as real DOM manipulation are expensive.
- It follows unidirectional data binding or data flow.
- It uses reusable or composable UI components for developing the view.

### Advantages of React?
- **Virtual DOM**: React uses Virtual DOM to render the view. As the name suggests, virtual DOM is a virtual representation of the real DOM. Each time the data changes in a react app, a new virtual DOM gets created. Creating a virtual DOM is much faster than rendering the UI inside the browser. Therefore, with the use of virtual DOM, the efficiency of the app improves.
- **Reusable components**: React uses component-based architecture of developing applications. Components are independent and reusable bits of code. These components can be shared across various applications having similar functionality. The re-use of components increases the pace of development.
- **SEO friendly**: React allows developers to develop engaging user interfaces that can be easily navigated in various search engines. It also supports server-side rendering, which boots the SEO of an app.
- **Huge ecosystem of libraries**: React provides you with the freedom to choose the tools, libraries, and architecture for developing an application based on your requirement.
- **Gentle learning curve**: React has a gentle learning curve when compared to frameworks like Angular. Anyone with little knowledge of Javascript can start building web applications using React.

### Limitations of React?
- React is not a full-blown framework as it is only a library.
- The components of React are numerous and will take time to fully grasp the benefits of all.
- It might be difficult for beginner programmers to understand React.
- Coding might become complex as it will make use of inline template and JSX.

### What is useState() in React?
The `useState()` is a built-in React Hook that allows us for having state variables in functional components. It declares a `state variable`. The only argument to the `useState` Hook is the initial state. It returns a pair of values: the current state and a function that updates it. Normally, variables disappear when the function exits but state variables are preserved by React.

### What are keys in React?
A key is special string attribute that needs to be included when using lists of elements.
- Keys help react identify which elements were added, updated or removed.
- Without keys, React does not understand the order or uniqueness of each element. 

### What is JSX?
JSX is a syntax extension to Javascript which provides a way to structure component rendering. It allows us to write HTML inside Javascript and place them in the DOM. React doesn’t require using JSX.
- Embedding Expression in JSX
    You can put any valid Javascript expression inside the curly braces in JSX.
    Examples:
    ```Javascript
    const name = 'Josh Perez';
    const element = <h1>Hello, {name}</h1>;
    ```
- JSX is an Expression Too
- Specifying Attributes with JSX
- JSX prevents injection attacks

    By default, React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application.
- JSX Represents Objects

    Babel compiles JSX down to React.createElement() calls.

### Differences between functional and class components?
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



### About Virtual DOM
Virtaul DOM is a concept where a virtual representation of the real DOM is kept inside the memory and is synced with the real DOM.

**Why virtualDOM introduced?**

DOM manipulation is an integral part of any web application, but DOM manipulation is quite slow when compared to other operations in Javascript. The efficiency of the application gets affected when several DOM manipulations are being done. Most Javascript frameworks update the entire DOM even when a small part of the DOM changes. For example, consider a list that is being rendered inside the DOM. If one of the items in the list changes, the entire list gents rendered again instead of just rendering the item that was updated. This is called inefficient updating. To address the problem of inefficient updating, the react team introduced the concept of virtual DOM.

**How does it work?**

For every DOM object, there is a corresponding Virtual DOM object, which has the same properties. The main difference between the real DOM object and the virtual DOM object is that any changes in the virtual DOM object will not reflect on the screen directly. Whenever a JSX element get rendered, every virtual DOM object gets updated. React uses two virtual DOMs to render the user interface. One of them is used to store the current state of the objects and the other to store the previous state of the objects. Whenever the virtual DOM gets updated, react compares the two virtual DOMS and gets to know about which virtual DOM objects were updated. After knowing which objects were updated, react renders only those objects inside the real DOM instead of rendering the complete real DOM. This way, with the use of virtual DOM, react solves the problem of inefficient updating.




### Differences between controlled and uncontrolled components
**Controlled Component**: In a controlled component, the value of the input element is controlled by React. We store the state of the input element inside the code, and by using event-based callbacks, any changes made to the input element will be reflected in the code as well. When a user enters data inside the input element of a controlled component, `onChange` function gets triggered and inside the code, we check whether the value entered is valid or invalid. If the value is valid, we change the state, and re-render the input element with the new value.

**Uncontrolled component**: In an uncontrolled component, the value of the input element is handled by the DOM itself. Input elements inside uncontrolled components work just like normal HTML input form elements. The state of the input element is handled by the DOM. Whenever the value of the input element is changed, event-based callbacks are not called. Basically, react does not perform any action when there are changes made to the input element. Whenever a user enters data inside the input field, the updated data is shown directly. To access the value of the input element, we can use **ref**.

### Explain React state and props
**React Props**: Every React component accepts a single object argument called props. These props can be passed to a component using HTML attributes and the component accepts these props as an argument. Using props, we can pass data from one component to another.

**React State**: Every component has a built-in state object, which contains all the property values that belong to that component. In other words, the state object controls the behavior of a component. Any change in the property values of the state object leads to the re-rendering of the component. State object is not available in functional components but, we can use React Hooks to add state to a functional component.

**Differences**:
- Props are immutable while state object are mutable. Props cannot be manipulated or changed inside a component.
- Props Has better performance than state. 
- State object is owned by the component, locally scoped.
- Changes to state can be asynchronous.

### Explain about types of side effects in React Component
There are 2 types of side effects in React component.

**Effects without Cleanup**: Network requests, manual DOM mutations, and logging are common examples of effects that don’t require a cleanup.

**Effects with Cleanup**: Some of the Hook effects will require the cleanup after updating of DOM is done.
For example, if you want to set up an external data source subscription, it requires cleaning up the memory else there might be a problem of memory leak.
It is a known fact that React will carry out the cleanup of memory when the unmounting of components happens.
But the effects will run for each render() method rather than any specific method.
This is why React also clean up effects from the previous render before running the effects next time.

### What is prop drilling in React?
Prop drilling is the unofficial term for passing data through several nested children components.
Sometimes while developing React applications, there is a need to pass data from a component that is higher in hierarchy to a component that is deeply nested.
To pass data between such components, we pass props from a source component and keep passing the prop to the next component in the hierarchy till we reach the deeply nested component.

### What are error boundaries?
Error boundaries are React components that catch Javascript errors anywhere in their child components tree, log those errors, and display a fallback UI instead of the component tree that crashed.
A JavaScript error in a part of the UI shouldn’t break the whole app.
To solve this problem for React users, React 16 introduces a new concept of an “error boundary”.
Error boundaries catch errors during
- rendering, 
- in lifecycle methods, 
- and in constructors of the whole tree below them.

Error boundaries do not catch errors for
- Event handlers
- Asynchronous code
- Server side rendering
- Errors thrown in the error boundary itself

A class component becomes an error boundary if it defines either of the lifecycle methods `static getDerivedStateFromError` or `componentDidCatch`.
Only class component can be error boundaries. Error boundaries only catch errors in the components below them in the tree.

### Explain React Hooks?
React Hooks are built-in functions that let us hook into React state and lifecycle methods from a functional component.
Previously, functional components were called stateless components. Only class components were used for state management and lifecycle methods.
Before React 16.8, it required a class component for managing the state of a component.
Using Hooks, all features of React can be used without writing class components.
Using `useState` hook, we can keep the state in a functional component.

There are 2 rules which must be followed while you code with Hooks:
- React Hooks must be called only at the top level. It is not allowed to call them inside the nested functions, loops or conditions
- It is allowed to call the Hooks only from functional components.

### What is the use of useEffect React Hooks?
The `useEffect` React Hook is used for performing the side effects in functional components.
With the help of `useEffect`, you will inform React that your component requires something to be done after rendering the component or after the state changes.
The function you have passed will be remembered by React and be called after DOM is updated.
Using this, we can perform various calculations such as data fetching, manipulating DOM directly, etc.
The `useEffect` hook will run by default after the first render and also after each update of the component.
The `useEffect` hook will accept 2 arguments.
The first argument represents the callback function having the logic of side-effect and it will be immediately executed after changes are made to DOM.
The second argument represents an optional array of dependencies. 
The `useEffect` will execute the callback only there is a change in dependencies between renderings.

### Why do React Hooks make use of refs?

### What are Custom Hooks
A custom hook is a function in Javascript whose name begins with `use` and that may call other hooks.
It allows us for reusing stateful logic without component hierarchy restructuring.
Traditionally in React, there are 2 popular ways to share stateful logic between components:
- render props
- higher-order components

In almost all the cases, custom hooks are considered to be sufficient for replacing these 2 methods and reducing the amount of nesting required.
Custom Hooks will allow you for avoiding multiple layers of abstraction or wrapper hell that might come along with these 2 methods.

The disadvantage of Custom Hooks is it cannot be used inside class components.

### Explain Strict Mode in React
StrictMode is a tool to highlight potential problems in an application.
It performs additional checks on the application.


### How to prevent re-renders in React?
Re-rendering of a component and its child components occur when props or the state of the component has been changed.
Re-rendering components that are not updated affects the performance of an application.
Any change in the parent component will lead to re-rendering of the child components as well.
To prevent the re-rendering of the child components, we use the `shouldComponentUpdate` method.

### What are the different ways to style a React component?
- **Inline Styling**: We can directly style an element using inline style attributes. 
- **Using Javascript object**: We can create a separate Javascript object and set the desired style properties.
- **CSS Stylesheet**: We can create a separate CSS file and write all the styles for the component inside that file.
- **CSS Modules**: We can create a separate CSS module and import this module inside our component.

### Techniques to optimize React app performance
- **useMemo()**:
Sometimes in a React app, a CPU expensive function gets called repeatedly due to re-renders of a component, which can lead to slow rendering.
useMemo() hook can be used to cache such functions. By using useMemo(), the CPU-Expensive function gets called only when it is needed.
- **React.PureComponent**
It is a base component class that checks the state and props of a component to know whether the component should be updated.
Instead of using the simple React.Component, we can use React.PureComponent to reduce the re-renders of a component unnecessarily.

- **Maintaining State Colocation**:
This is a process of moving the state as close to where you need it as possible. 
Sometimes in React app, we have a lot of unnecessary states inside the parent component which makes the code less readable and harder to maintain.
Having many states inside a single component leads to unnecessary re-renders for the component.
It is better to shift states which are less valuable to the parent component, to a separate component.

- **Lazy loading**:
It is a technique to reduce the load time of a React app.
Lazy loading helps reduce the risk of web app performances to a minimum.

### How to pass data between react components
React follows unidirectional data binding or data flow.

- We can pass data from a parent Component to the Child Component using props.
- We can pass data from a child component to the parent component using callback.
Create a callback in the parent component which takes in the data needed as a parameter.
Pass this callback as a prop to the child component.
Send data from the child component using callback.

### What are Higher Order Components?
Simply put, Higher-Order Component(HOC) is a function that takes in a component and returns a new component.

While developing React applications, we might develop components that are quite similar to each other.
In most cases, developing similar components might not be an issue but while developing larger applications we need to keep our code DRY,
therefore, we want an abstraction that allows us to define this logic in a single place and share it across components.
HOC allows us to create that abstraction.

### What are the different phases of the component lifecycle?
There are 4 different phases in the lifecycle of React component. 
- **Initialization**: During this phase, React component will prepare by setting up the default props and initial state.
- **Mounting**: Mounting refers to putting the elements into the browser DOM.
Since React uses virtualDOM, the entire browser DOM which has been currently rendered would not be refreshed. This phase includes lifecycle methods `componentWillMount` and `componentDidMount`
- **Updating**: In this phase, a component will be updated when there is a change in the state or props of a component. This phase will have lifecycle methods like `componentWillUpdate`, `shouldComponentUpdate`, `render` and `componentDidUpdate`.
- **Unmounting**: In the last phase of the component lifecycle, the component will be removed from the DOM or will be unmounted from the browser DOM. This phase will have the lifecycle method named `componentWillUnmount`.

### What are the lifecycle methods of React?
React lifecycle hooks have the methods that are automatically called at different phases in the component lifecycle.
It provides the power to effectively control and manipulate what goes on throughout the component lifecycle.

- `constructor`: will be called when the component is initiated before anything has been done. It helps to set up the initial state and initial values.
- `getDerivedStateFromProps`: This method will be called just before elements rendering in DOM. It helps to set up the state object depending on the initial props. This method will have a state as an argument, and it returns an object that made changes to the state. This will be the first method to be called on an updating of a component.
- `render`: This method will output or re-render the HTML to the DOM with new changes.
- `componentDidMount`: This method will be called after the rendering of the component.
- `shouldComponentUpdate`: This method will specify whether React should proceed further with rendering or not by returning boolean value.
- `getSnapshotBeforeUpdate`: This method will provide access to props as well as state before the update. 
- `componentDidUpdate`: This method will be called after the component has been updated in the DOM.
- `componentWillUnmount`: This method will be called when the component removal from the DOM is about to happen.

### Does React Hook work with static typing?
Static typing refers to the process of code check during the time of compilation for ensuring all variables will be statically typed.
React Hooks are functions that are designed to make sure about all attributes must be statically typed.
For enforcing stricter static typing within our code, we can make use of the React API with custom Hooks.

### Explain about types of Hooks in React.

- Basic Hooks:
  - `useState`: This allows us for having state variables in functional components .
  - `useEffect`: It enables for performing the side effects in the functional components.
  - `useContext`: It is used for creating common data that is to be accessed by the component hierarchy without having to pass the props down to each level.
- Additional Hooks
  - `useReducer`: 
  - `useMemo`
  - `useCallback`
  - `useImperativeHandle`
  - `useDebugValue`
  - `useRef`
  - `useLayoutEffect`
  
### What is React Router?
React Router refers to the standard library used for routing in React.
It permits us for building a single-page-web application in React with navigation without even refreshing the page when the user navigates.
It also allows to change the browser URL and will keep the user interface in sync with the URL.
React Router will make use of the component structure for calling the components, using which appropriate information can be shown.
Since React is a component based framework, it's not necessary to include and use this package.
