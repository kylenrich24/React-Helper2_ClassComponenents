# 🌀 React-Helper3_Class Componenents 🌀

<img src="https://sunscrapers.com/blog/wp-content/uploads/2018/11/1__DOHv30w-0eI-Ysz5U47Yg.png" height=500 width=900>

<h2>🌀 Class-Based Components</h2>
<br>
 <img src="https://www.techdiagonal.com/wp-content/uploads/2019/08/React-components-blog-image.jpg" height=350 width=350> 
<br>

To generate a functional component in VSCode: <em>rcc</em>
<br>
<br>


&nbsp;🌀&nbsp; Functional Component - good for simple content without logic behind it <br>
&nbsp;🌀&nbsp; Class-Based Component - good for everything else


<ul>
 <li>Easier code organization</li>
 <li>State - &nbsp;&nbsp; easier to handle user input</li>
 <li>Lifecycle Events - &nbsp;&nbsp;  easier to do things when app first starts</li>
</ul>
<br>
<br>

```jsx
import React, {Components} from 'react'

class SeasonDisplay extends Components {
 render() {                              // the only requirement of a class function is to have a render method
  return (
   <div></div>
   )
 }
}

export default SeasonDisplay
```

<br>
<br>
<h2>🌀 State</h2>
<br>
&nbsp;🌀&nbsp; JS object that contains data relevant to a component <br>
&nbsp;🌀&nbsp; Updating state on a component causes the component to rerender <br>
&nbsp;🌀&nbsp; State must be initialized when a component is created <br>
&nbsp;🌀&nbsp; State can only be updated with setState()<br>
<br>
<br>

using state

```jsx
class SeasonDisplay extends Component {
 constructor(props) {                // we are overwriting our parents constructor
  super(props)                       // retaining our parents constructor and just adding to it
  this.state = {lat: null }          // our state; initializing it to null because we're expecting a number 
  
  getLocation(
   position => this.setState ({lat: position.latitude})    // changing our state
  )
 }
 
 render() {                     // required for a class component
  return JSX
 }
}
```

<br>
<br>
<h2>🌀 Lifecycle Methods</h2>
<br>
<p>These are methods in our Class-Based Components. React automatically call them at certain points during a components lifecycle. A component's lifecycle goes like this: gets created, shows up in DOM, rerender and in theory gets removed in the DOM altogeher </p>
<p>For instance after render(), componentDidMount() gets called one time after our component gets rendered in our screen. We can put some codes here for our component setup.</p>
<br>
&nbsp;🌀&nbsp;&nbsp; constructor - good place to do one-time setup<br>
&nbsp;🌀&nbsp;&nbsp; render - only for returning JSX<br>
&nbsp;🌀&nbsp;&nbsp; componentDidMount - good place to do data loading<br>
&nbsp;🌀&nbsp;&nbsp; componentDidUpdate - good place to do more data-loading when state/props change<br>
&nbsp;🌀&nbsp;&nbsp; componentWillUnmount - good place to do cleanup<br>
<br>

<br>
<img src="https://cdn-media-1.freecodecamp.org/images/NpWCjYyzfnJkn7rXwDmyWwK2DqInFJu6-g1O" height=400 width=300>
<br>
<br>

```jsx
class App extends Component{
 
 state={ lat: null}                                        // this is an easier alternative for initializing state; Babel
 
 componentDidMount(){                                      // we take care of data loading here
  getLocation(
   position => this.setState ({lat: position.latitude})    // changing our state
  )
 }
 
 render() {
  return <div>{this.state.lat}</div>
 } 
}

export default App
```

<br>
<h2>🌀&nbsp;Ref System</h2>
<br>

Getting a DOM element in React

```jsx
 constructor(props) {                       // we create the ref in the constructor
    super(props);

    this.imageRef = React.createRef();
  }
 
 render() {
  return (
   <img ref={this.imageRef} />             // we pass the createf ref to <img />; we get the <img />
  )
 }
```
