# Reactive

* Iterator: Sequentially access the elements of a collection without knowing the inner workings of the collection.  
* Observer: A way of notifying change to a number of classes to ensure consistency between the classes.

Iterator

```javascript
//ES 6

var iterator = ["apple", "oranges", "banana"];        
<-:undefined   

var fruits = iterator[Symbol.iterator]();
<:-undefined

> fruits.next()
<:-{value: "apple", done: false}

> fruits.next()
<:-{value: "oranges", done: false}

>fruits.next()
<:-{value: "banana", done: false}

>fruits.next()
<:-{value: undefined, done: true}
```

### 

### Observables:

Observables helps in modeling 

* Events
* Async Requests
* Animations 

We can use Observables as replacement for

* Dom Events
* setIntervals
* XMLHttpRequests
* WebSockets
* Node Streams
* Service Workers



