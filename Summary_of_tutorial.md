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

### Best Practices
- To save typing and avoid the confusing behavior of this, we will use the arrow function syntax for event handlers
- use 'string', not "string"
- one HTML argument per line:
  ```jsx
    <button
       className="square"
       onClick={() => this.setState({value: 'X'})}
    >
  ```
