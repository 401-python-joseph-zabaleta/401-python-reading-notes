# Reading Notes 38  

## Articles  

### React - Conditional Rendering  
* [Link to Article](https://reactjs.org/docs/conditional-rendering.html)  

Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

```js
function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}

function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}

ReactDOM.render(
  // Try changing to isLoggedIn={true}:
  <Greeting isLoggedIn={false} />,
  document.getElementById('root')
);

```

### React - Lists & Keys  
* [Link to Article](https://reactjs.org/docs/lists-and-keys.html)  

Rending a list is as follows:
```js
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li>{number}</li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity:
```js
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li key={number.toString()}>
    {number}
  </li>
);
```


### React - Forms  
* [Link to Article](https://reactjs.org/docs/forms.html)  

Example Form:
```js
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

### React - Lifting State  
* [Link to Article](https://reactjs.org/docs/lifting-state-up.html)  

Often, several components need to reflect the same changing data. It's recommended, lifting the shared state up to their closest common.  

### React - Composition vs Inheritance  
* [Link to Article](https://reactjs.org/docs/composition-vs-inheritance.html)  

React has a powerful composition model, and they recommend using composition instead of inheritance to reuse code between components.  
Some components don't know their chieldn ahead of time. There is a special children prop to pass children directly into their outputs. Example:  
```js
function FancyBorder(props) {
  return (
    <div className={'FancyBorder FancyBorder-' + props.color}>
      {props.children}
    </div>
  );
}
```

### Thinking in React  
* [Link to Article](https://reactjs.org/docs/thinking-in-react.html)  

## Bookmark/Skim  
* [React - Comprehensive Guide](https://tylermcginnis.com/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)