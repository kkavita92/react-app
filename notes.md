## Notes

# When square is clicked
```
class Square extends React.Component {
  render() {
    return (
      <button className="square" onClick={() => this.props.onClick()}>
        {this.props.value}
      </button>
    );
  }
}
```
* ```onClick``` prop on <button> component tells React to set up a click event listener
* When button is clicked, React will call the ```onClick``` event handler defined in Square's render() method
* This event handler calls this.props.onClick().
* Since Board has passed ```onClick={() => this.handleClick(i)}```, it runs ```this.handleClick(i)``` on the Board.
* Square no longer keeps its own state -> it receives value from its parent Board and informs its parents when it's clicked (controlled components)

# Benefit of Immutability in React
* Comes when building simple pure components
* Since immutable data can more easily determine if changes have been made -> helps to determine when component requires re-rendering

# Keys
* When you render a list of items, React stores some info about each item in list
* If you render a component that has state, state needs to be stored
* When you update that list, React needs to determine what has changed
* For that purpose, React asks you to specify a key property on each element in a list to differentiate each component from its siblings  --> if items corresponds to database objects, database ID would be a good choice
* React uses key automatically while deciding which children to update
* No way for a component to inquire about its own key BUT keys tell React about identity of each component so that it can maintain state across re-renders.

# Misc
* You can set up initial state by adding a constructor to class
