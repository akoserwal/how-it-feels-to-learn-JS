# Understanding the Basic

Let's begin with understanding basic concepts of JavaScript.

**Variables:** number, string, boolean, null, undefined, objects.

![variable](/images/variable.png)To define a variable of any type use keyword.

> `var nameOfVariable = (assignment operator) Value ;`
>
> `(; is must. Chrome, Firefox understand your emotions & ignores bad habit missing ; for testing purpose)`

This is different from strongly-typed programming languages liked  C, C++ or Java. Where the type-checking at compile time as opposed to dynamically typed languages \(run-time checking\) like JavaScript as shown in the above figure using Chrome V8 run-time. I would highly recommend to try this examples in your browser console.

> `var a = 5;`
>
> `<- undefined; (return type)`

Value return by run-time is of type `undefined.`While in-case of using operator `typeof(argument)`returns string `"number".`Declaration of a variable does not return any value that is why it returned with type `undefined.`Evaluated variable does not have a assigned value or defined return type; then it will return `undefined`_. _

You can override the value with any type of variable type. This seems bit odd and sounds type unsafe while working with a large code base. Using`var`keyword again would define a new variable in the memory space.  Browser gives the intellisense about available properties and methods as shown in the figure.

![](/assets/Screenshot from 2017-06-26 22-18-34.png)

