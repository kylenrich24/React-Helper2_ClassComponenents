# 🌀 React-Helper3_Class Componenents 🌀

<img src="https://sunscrapers.com/blog/wp-content/uploads/2018/11/1__DOHv30w-0eI-Ysz5U47Yg.png" height=500 width=900>

<h2>🌀 Class-Based Components</h2>
<br>
 <img src="https://www.techdiagonal.com/wp-content/uploads/2019/08/React-components-blog-image.jpg" height=350 width=350> 
<br>

To generate a functional component in VSCode: <em>rcc</em>
<br>

<br>
<br>


<h2>Functional Component</h3>
<br>
To generate a functional component in VSCode: <em>rafce</em>
<br>
<br>
CommentDetail Component:

```jsx
import React from 'react'

const CommentDetail = () => {
    return (      // functional component always have a return 
        <div>     // it returns JSX
            
        </div>
    )
}

export default CommentDetail

```
<br>
<h3>Reusable and Nesting Component</h3>
<br>

```jsx
import CommentDetail from './CommentDetail'

const App = () => {
 return (
  <div>
    <CommentDetail />  // our component
    <CommentDetail />
    <CommentDetail />
  <div>
 )
}

export default App
```
<br>
<br>
<h2>Props System</h2>
<br>
&nbsp; 🌀 &nbsp; System for passing data from a parent to a child<br>
&nbsp; 🌀 &nbsp; Configures and customizes child components<br>
<br>
<br>
<img src="https://www.techdiagonal.com/wp-content/uploads/2019/09/react-props-blog-image-design-2.jpg" height=350 width=350> 
<br>
<h3>Passing and Receiving Props</h3>
<br>

Passing props 
<br>

```jsx
const App = () => {
 return (
  <div>
    <CommentDetail author="Sam" picture="url1"/>  // passing props
    <CommentDetail author="Bob" picture="url2"/>
    <CommentDetail author="John" picture="url3"/>
  <div>
 )
}
```
<br>
Receiving props 
<br>
<br>

```jsx
const CommentDetail = (props) => {
 return (
  <div>
   <div>
    <img src={props.picture}>  // props
   </div>
    <h1>{props.author}</h1>  // props
  <div>
 )
}
```
<br>
<h3>Children Props</h3>
<br>

```jsx
return (
 <ApprovalCard>
  <CommentDetail />
 </ApprovalCard/>
 <ApprovalCard>
  Hello There!
 </ApprovalCard/>
)
```
<br>

```jsx
const ApprovalCard = (props) => {
  return (
    <div>
      {props.children}   // children here
      <div>
        <button>Click Me</button>
      </div>
    </div>
  );
};
```


