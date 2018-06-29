# Anonymous Function

An anonymous function is a function [literal](https://en.wikipedia.org/wiki/Literal_%28computer_programming%29) without a name, while a closure is an instance of a function

Concept derived from functional paradigm & common to various languages. As from the name anonymous function we can deduce that function without a name identifier. it is a function literal which can be assigned to any variable identifier.

Understand with a example

```javascript
var getName = function(name) { return name; }


> getName
-> ƒ (name) { return name; }   // function literal 

> getName("John")
<-: "John"

> var name = getName;

> var myname = getName;
<- undefined
> myname("Jack")
<-: "Jack"
```

You can't do such thing with most of the strongly typed languages, anonymous function are used more as a lambda function in most of strongly type languages.

