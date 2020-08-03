# React

React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It lets you compose complex UIs from small and isolated pieces of code called “components”.

To create a new app: `npx create-react-app tic-tac-toe`

## Component
```jsx
class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}

// Example usage: <ShoppingList name="Mark" />
```

A component subclass describe a piece of a web page. When our data changes, React will efficiently update and re-render our components.

A component takes in parameters, called `props` (short for “properties”) and has the method `render` that returns a description of what you want to see on the screen.

Every component has a variable `state`, that can be updated with method `setState`.

Every component can have a `constructor` (with argument `props`), whose first line is always `super(props)`.

### Function components
Function components are a simpler way to write components that only contain a render method and don’t have their own state. They are a function that takes props as input and returns what should be rendered.

```jsx
function Square(props) {
  return (
    <button className="square" onClick={props.onClick}>
      {props.value}
    </button>
  );
}
```

## Best Practices
- To save typing and avoid the confusing behavior of this, we will use the arrow function syntax for event handlers
- use 'string', not "string"
- one HTML argument per line:
  ```jsx
    <button
       className="square"
       onClick={() => this.setState({value: 'X'})}
    >
  ```
- usually the state stay in the parent component (and he passes the value and an update function using `prop`)
- it’s conventional to use on[Event] names for props which represent events and handle[Event] for the methods which handle the events
-  Immutability Is Important
    - Avoiding direct data mutation lets us keep previous versions of the game’s history intact, and reuse them later
    - Detecting changes in immutable objects is considerably easier
    - Immutable data can easily determine if changes have been made, which helps to determine when a component requires re-rendering.