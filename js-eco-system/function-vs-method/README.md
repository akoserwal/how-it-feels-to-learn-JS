# Function vs Method

In mathematics, a function is a relation between a **set of inputs** and a **set of permissible outputs** with the property that **each input** is related to **exactly one output**. \(Wikipedia\)

Mathematical expression: x \(input\), y\(permissible output\)

```javascript
y = f(x)
```

JavaScript function for above mathematical expression

```javascript
 var y = function(x) { return x; } //called as Anonymous function
```

Generic way to define a function:

> function nameofFunction \( \) { //body return something or //perform some action}

Let's define a simple function to understand the above definition in terms of JavaScript.

```javascript
> function add(x,y) { return x+y; }
<-: undefined

> typeof(add) //operand typeof
<-:"function"

> add(2,3)   //number
<-: 5

> add("Hello","World")  //string
<-: "HelloWorld"  //string

> add([1,3],[7,8])  // array
<-: "1,37,8"  // string

> add(true, false)  //passing boolean
<-: NaN         //Not a Number, as + operation can't be performed over boolean.
```

> So, we can see from the above examples for each set of input like number, string, array etc. add function returned with the permissible output. For boolean input the function return NaN: Not a Number.

Now to understand difference between a method and a function is related to context. Under the hood, both suppose to perform given task or operation. If a function operating over the properties & defined within the scope of a Object; we will refer it as method. If it defined in the general context to perform operation like above example add; we will refer it as function.

Let's take the previous example

```javascript
var person = {
                "firstName":"John", // Property
                "lastName":"Wick", // Property
                "getFullName": function(){ // Method
                                return this.firstName + this.lastName; 
                             }
             };
```

We can call _add function direclty, but to call getFullName_. We need Object reference of variable _person_.

