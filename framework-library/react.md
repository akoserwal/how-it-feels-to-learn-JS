---
description: JS Library
---

# React

React is developed by Facebook & open sourced it. It follows functional paradigm over object oriented approach. 

Let's see how hello world looks like in react vs pure Javascript

#### React 

```markup
// html
<div id="root"></div>
```

```jsx
//script
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

> #### Vanilla JavaScript using DOM API

```javascript
  // create a new div element 
  var divTag = document.createElement("div"); 
  // and give it some content 
  var contentNode = document.createTextNode("Hello World"); 
  // add the text node to the newly created root div
  divTag.appendChild(contentNode);  
```



