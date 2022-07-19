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
- [Explain Strict Mode in React](#)
- [How to prevent re-renders in React?](#)
- [What are the different ways to style a React component?](#)
- [Techniques to optimize React app performance](#)
- [How to pass data between react components](#)
- [What are Higher Order Components?](#)


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

**Effects with Cleanup**:

### What is prop drilling in React?

### What are error boundaries?

### Explain React Hooks?

### What is the use of useEffect React Hooks?

### Why do React Hooks make use of refs?

### What are Custom Hooks
