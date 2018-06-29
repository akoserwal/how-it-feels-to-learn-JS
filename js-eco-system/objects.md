# Objects

Term "object" will seems familiar if you are coming from object oriented programming background. Most common description of an object is "object referred as an instance of class". But there is no such concept of classes in JavaScript although word 'class' is a reserved keyword. That is been introduced in ECMAScript 6 version. Which will be cover later in this book. This doesn't mean you can't implement object oriented paradigm in JavaScript. It can be achieved by constructor functions.

JavaScript objects are a collection of properties and methods that could be a variable, function, method & data structure. let's revisit the example that we have discussed in the previous section.

```javascript
> var d = [];
<-:undefined
> typeof(d);
<-:"object"

> var e = {};
<-:undefined
> typeof(e);
<-:"object"

> var f = null;
<-:undefined
> typeof(f);
<-:"object"
```

Which one of the above variable should be called as an object? as a type of operand returns "object" for all three variables. Let's talk about the first \(d\) and last \(f\). Which is called as "Mistake" by Douglas Crockford or bad parts of the JavaScript.

First one is syntax we used for defining Array in JavaScript. Although it meets the above description about an object. but about the last example. It is not well justifiable to be called as an object. As fixing this could break existing follow of the application.

To test for a null value

```javascript
> var f = null;

> (!f && typeof f === 'object') 
<-: true
```

Now the middle one, this is way to declare objects in JavaScript.

```javascript
var e = {}; //object literal notation
```

Another way to declare object.

```javascript
var e = new Object();
```

It is like a container with properties & methods; defined 'key/value' pair.

```javascript
> var person = { 
                 "firstName":"John",           // Property
                 "lastName":"Wick",            // Property
                 "getFullName": function(){    // Method
                                  return this.firstName + this.lastName; 
                  } 
               }; 
<-:undefined

> person;
<-:Object {firstName: "John", lastName: "Wick", getFullName: function}

> person.firstName;  // Access object property using key
<-:"John"

> person["firstName"]  // Another way to access like array
<-:"John"

> person.getFullName() // Calling method
<-:"JohnWick"
```

Few new things introduced with person object.

* **method** : getFullName\(\)
* **keyword** `this & concept of scopes`

We will cover object oriented aspect in coming section **Programming paradigm.**

