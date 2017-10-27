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

# Storing Game History
* Already creating a new ```squares``` array each time a move is made -> immutable

# Misc
* You can set up initial state by adding a constructor to class
