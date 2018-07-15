# Reactive

> **ReactiveX is a combination of the best ideas from  
> the Observer pattern, the Iterator pattern, and functional programming**

### Iterator pattern

> Iterator: Sequentially access the elements of a collection without knowing the inner workings of the collection.

```javascript
//ES 6

var iterator = ["apple", "oranges", "banana"];        
<-:undefined   

var fruits = iterator[Symbol.iterator]();
<:-undefined

> fruits
Array Iterator {}
ƒ next()
Symbol(Symbol.toStringTag)
"Array Iterator"

> fruits.next()
<:-{value: "apple", done: false}

> fruits.next()
<:-{value: "oranges", done: false}

>fruits.next()
<:-{value: "banana", done: false}

>fruits.next()
<:-{value: undefined, done: true}
```

### Observer pattern

> Observer: A way of notifying change to a number of classes to ensure consistency between the classes.

```javascript
var Subject = function() {
  var self = this;
  self.observers = [];
  
  return {
    subscribe: function(observer) {
      self.observers.push(observer);
    },
    unsubscribe: function(observer) {
      var index = self.observers.indexOf(observer);
      if (index > -1) {
        self.observers.splice(index, 1);
      }
    },
    notify: function(observer) {
      var index = self.observers.indexOf(observer);
      if (index > -1) {
        self.observers[index].notify(index);
      }
    },
    notifyAll: function() {
      for (var i = 0; i < self.observers.length; i++) {
        self.observers[i].notify(i);
      }
    }
  };
};

var Observer = function() {
  return {
    notify: function(index) {
      console.log("Observer " + (index+1) + " is notified!");
    }
  }
}

  var subject = new Subject();
  
  var observer1 = new Observer();
  var observer2 = new Observer();
  var observer3 = new Observer();

  subject.subscribe(observer1);  
  //"Observer 1 is notified!"
  subject.subscribe(observer3);  
  // no output
  
  subject.notifyAll();
  //"Observer 1 is notified!"
  //"Observer 2 is notified!"
```

### 

### Let's try to combine both patterns

```javascript
var Subject = function() {
  var self = this;
  self.observers = [];

  return {
    subscribe: function(observer) {
      self.observers.push(observer);
    },
    unsubscribe: function(observer) {
      var index = self.observers.indexOf(observer);
      if (index > -1) {
        self.observers.splice(index, 1);
      }
    },
    notify: function(observer) {
      var index = self.observers.indexOf(observer);
      if (index > -1) {
        self.observers[index].notify(index);
      }
    },
    notifyAll: function() {
      for (var i = 0; i < self.observers.length; i++) {
        self.observers[i].notify(i);
      }
    },
    notifyIterator: function() {
        var i = 0;
        return {
            next: function(){
               return i < self.observers.length ?
               {value: self.observers[i++].notify(i), done: false}:
               {done: true};
            }
        };
    }
  };
};

var Observer = function() {
    return {
      notify: function(index) {
        console.log("Observer " + (index) + " is notified!");
      }
    }
  }
  
  var subject = new Subject();
  
  var observer1 = new Observer();
  var observer2 = new Observer();


  subject.subscribe(observer1);  
  subject.subscribe(observer2);  
  

var it = subject.notifyIterator();
 it.next().value;
 it.next().value;
 it.next().done;
// output
"Observer 1 is notified!"
"Observer 2 is notified!"
true
```

Try out: [jsbin](https://jsbin.com/viqeled/edit?js,console)

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



