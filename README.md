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

using state

```jsx
class SeasonDisplay extends Component {
 constructor(props) {                // we are overwriting our parents constructor
  super(props)                       // retaining our parents constructor and just adding to it
  this.state = {lat: null }          // our state; initializing it to null because we're expecting a number 
 }
 
 render() {                     // required for a class component
  return JSX
 }
}
```

