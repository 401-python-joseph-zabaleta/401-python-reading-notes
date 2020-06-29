# Reading Notes 37  

## Articles  

### ES6 Syntax and Feature Overview
* [Link to Article](https://www.taniarascia.com/es6-syntax-and-feature-overview/)  

#### Variable declaration  
```js
// ES5
var x = 0

// ES6
let x = 0
```

#### Constant declaration  
```js
// ES6
const CONST_X = 0 // constants are uppercase by convention  
```

#### Arrow Functions // Implicit returns
```js
// ES5
var myFunction = function func(a, b, c,) {
    return (a + b + c)
}

// ES6
let function = (a, b, c) => (a + b + c) // curly brackets must be ommitted
```

#### Template literals  
```js
// ES5
var str = 'Release date: ' + date

// ES6
let str = `Release Date: ${date}`
```

#### Multi-line Strings  
```js
// ES5
var str = 'This text ' + 'is on ' + 'multiple lines'

// ES6
let str = `This text
            is on
            multiple lines`
```
#### Key/property shorthand
```js
// ES5
var obj = {
  a: a,
  b: b,
}

// ES6
let obj = {
  a,
  b,
}
```

### React - Hello World  
* [Link to Article](https://reactjs.org/docs/hello-world.html) 
### React - JSX  
* [Link to Article](https://reactjs.org/docs/introducing-jsx.html) 

```js
const element = <h1>Hello, world!</h1>;
```
- This funny tag syntax is niether a string nor HTML, this is what we call JSX.  
- It is a syntax extension to JavaScript.  
- You can put any valid JavaScript expression inside the curly braces in JSX.  
- After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.  
- If a tag is empty, you may close it immediately with />, like XML  
- It is safe to embed user input in JSX  
- Babel compiles JSX down to React.createElement() calls.  
- React.createElement() performs a few checks to help you write bug-free code  
- These objects are called “React elements”. You can think of them as descriptions of what you want to see on the screen. React reads these objects and uses them to construct the DOM and keep it up to date.  

### React - Rendering Elements  
* [Link to Article](https://reactjs.org/docs/rendering-elements.html)  
- Elements are the smallest building blocks of React apps.  
- An element describes what you want to see on the screen.  
- Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.  

#### Rending an element into the DOM:  
`<div id="root"></div>`
```js
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
We have a root div, they will be managed by the React DOM. We pass in a React element into a root DOM node both into render().  

#### Updating the Rendered Element  
React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.  

#### React Only Updates What's Necessary  
React DOM compares the element and its children to the previous one, and only applies the DOM updates necessary to bring the DOM to the desired state.  

### React - Components & Props  
* [Link to Article](https://reactjs.org/docs/components-and-props.html)  

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.  

### React - State & Lifecycle  
* [Link to Article](https://reactjs.org/docs/state-and-lifecycle.html)  
Converting a function into a class, ES6 that extends React.Component. This will be object orientated using this.props instead of props. 
- The componentDidMount() method runs after the component output has been rendered to the DOM. 
- the componentWillUnmount() method will tear down the lifecycle method.  

### React - Handling Events  
* [Link to Article](https://reactjs.org/docs/handling-events.html)  
Handling events with React elements is very similar to handling events on DOM elements. There are some syntax differences:
    - React events are named using camelCase, rather than lowercase.  
    - With JSX you pass a function as the event handler, rather than a string.

## Bookmark/Skim  
* [React - Installation](https://reactjs.org/docs/create-a-new-react-app.html)  
* [React - Comprehensive Guide](https://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)  
* [Understanding Variables, Scope, and Hoisting in JavaScript](https://www.digitalocean.com/community/tutorials/understanding-variables-scope-hoisting-in-javascript)  