---
description: JS Library
---

# React

React is developed by Facebook & open sourced it. It follows functional paradigm over object oriented approach. 

Let's see how hello world looks like in react vs pure Javascript

#### React 

Base JS files imports:

```markup
 <script src="react.development.js"></script> 
 <script src="react-dom.development.js"></script> 
 <script src="babel-browser.min.js"></script>
```

```markup
// html
<div id="root"></div>
```

```jsx
//script
<script type="text/babel">
ReactDOM.render(
  "Hello, world!",
  document.getElementById('root')
);
</script>
```

> #### Vanilla JavaScript using DOM API

```javascript
  // create a new div element 
  var divTag = document.createElement("div"); 
  // and give it some content 
  var contentNode = document.createTextNode("Hello World"); 
  // add the text node to the newly created div
  divTag.appendChild(contentNode);  
  // adding 'id' attribute with value "root" to div element. 
  divTag.setAttribute('id', "root");
```





