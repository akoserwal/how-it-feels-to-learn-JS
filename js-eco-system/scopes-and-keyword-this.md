# Scopes and keyword "this"

The concept of scopes can be understood in two major categories "Global" and "Local".

"this" is widely used in programming languages for the referencing the scope of an object like a pronoun.

```javascript
> this
<-:Window {speechSynthesis: SpeechSynthesis, caches: CacheStorage, localStorage: Storage, sessionStorage: Storage, webkitStorageInfo: DeprecatedStorageInfo…}
```

> Output of this here return 'Window' object. Which expose browser API in form of JavaScript Object. Context of this depends upon where it is called or used as a referenced. In future chapters we will see, the definition of \_this \_changes like if see console output in Node.js console, the output will be different.
>
> Window object is the reason for using JavaScript, as a language for performing any DOM modification.
>
> "Global" is a broad term. We need to drill down and pick up the smallest unit that blocks scoped.

**{Block Scope}**

Let's take the previous example of an object.

```javascript
var person = {
                "firstName":"John", // Property
                "lastName":"Wick", // Property
                "getFullName": function(){ // Method
                                return this.firstName + this.lastName; 
                             }
             };
```

As we now understand, we can't access firstName, lastname and getFullName directly. Due to person object created a block scope. We need an object reference to access properties/method. This ability may sound as close to "Encapsulation" concept if you are familiar with Object oriented paradigm.

```javascript
// Global Scope

var a = {
                //blocked scope or local scope.
};
```

To better understand this concept.

```javascript
function outer() { 
                   var a=1; 
                   function inner() { 
                    console.log(a); 
                   }
                   inner();
                 } 

> outer();
<-:1
> inner()
<-: Uncaught ReferenceError: inner is not defined
```

You can't call the inner\( \) function outside the outer\( \) function due to block scoping. Now assign

```javascript
var a = this;
//and call outer().

> outer();
Window {speechSynthesis: SpeechSynthesis, caches: CacheStorage, localStorage: Storage, sessionStorage:
"this" keyword is still referencing _Global Window _object. This may sound bit odd behaviour than compare to other languages.
```

"this" keyword is still referencing \_Global Window \_object. This may sound bit odd behaviour than compare to other languages.

```javascript
> var person = {
                "firstName":"John", // Property
                "lastName":"Wick", // Property
                "getFullName": function(){  console.log(this);
                                return this.firstName + this.lastName; 
                                }
             };


> person.getFullName();
 >> Object {firstName: "John", lastName: "Wick"}
<:-"JohnWick"
```

Here output of console.log\(this\) is giving a reference to person object.

