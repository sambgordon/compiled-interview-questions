<style> .head{ color: #70ffe6; } </style>

# Javascript Questions

<div class="head">

## What's **event delegation**?

</div>

**Event delegation** is when you **add event listeners to a parent element** instead of to the descendant elements. It allows you to **put a single event handler on a common ancestor** instead of assigning a handler to each element.

<div class="head">

## Explain how **this** works in JS

</div>

`this` is used to refer to the current object in the code. 

In the global execution context, `this` refers to the global object (strict mode or not).

<div class="head">

## Explain how **prototypal inheritance** works

</div>

A **prototype** is **a reference to another object**. In Javascript, every object has its prototype, meaning it's created from a prototype, which is created from it's own prototype, all the way until the end value which is `null`. If you analyze an object in the console you can actually follow this chain visually.

<div class="head">

## What do you think of **AMD** vs **CommonJS**?

</div>

Both are different ways to implement modules, which weren't available until **ES6**. 
**CommonJS** is **synchronous**, while **AMD** is **asynchronous** ("Asynchronous Module Definition").

**CommonJS** is **designed with server-side development in mind**, while **AMD** is for **asynchronous loading of modules** and is more intended for browsers.

<div class="head">

## Name some of the different methods used to convert non-numerical values into numbers

</div>

Three main ways:

* `parseInt()`
* `parseFloat()`
* `Number()`

<div class="head">

## What's the difference between **null**, **undefined**, and **undeclared**?

</div>

`Undeclared` - created when you assign something that's not previously created. Undeclared variables are defined globally, outside the current scope (throws a `ReferenceError`).

`Undefined` - a variable that's been **declared but not assigned a value**.

`Null` - It **can be assigned** to a variable to represent "no value"; so it's explicitly assigned. 

<div class="head">

## What's an **anonymous function**?

It's a function declared without any named identifier and **is not accessible after declaration**.

## What's a typical use case for **anonymous functions**?

</div>

It can be used for **callbacks**, especially **where something needs to be used once and not anywhere else**.

This way the code is more **self-contained** and readable.

<div class="head">

## How do you organize your code?

</div>

Usually **OOP**. I also take the **modular** approach. I only deal with **classes** when using React.

<div class="head">

## What's the difference between **host** objects and **native** objects?

</div>

**Native** objects - part of the JS language defined by the ECMAScript specification (String, etc).

**Host** objects - objects provided by the runtime environment (browser, Node). Examples are `window` object, **dom objects**, and `XMLHttpRequest`.

<div class="head">

## What are the roles of **break** and **continue** statements?

</div>

`Break` statements are used to come out of the current loop.

`Continue` statements continue the current loop **with a new recurrence**.

<div class="head">

## What is **namespacing** in Javascript and how is it used?

</div>

**Namespacing** is used for grouping functions, variables, etc. under a unique name. It's a name that's been attached to desired functions, objects, properties. Namespacing is used because it enables code reuse and modularity.

<div class="head">

## What's the difference between **.call** and **.apply**?

</div>

Both function similarly, but `.call` takes in **comma-separated** arguments while `.apply` takes in an **array** of arguments.

An easy way to remember: 

* **C**all = **C**omma-separated
* **A**pply = **A**rray-separated

<div class="head">

## How are object **properties** assigned in Javascript?

</div>

Similar to the way a value is assigned to a variable:

```js
document.form.action="submit"
```

<div class="head">

## Explain **closures**

</div>

A closure resembles an object, and it gets instantiated **whenever you call a function**.

The scope is **lexical**, meaning everything contained within the function which the closure belongs to has access to any variable that's in it.

<div class="head">

## Explain **Function.prototype.bind**

</div>

Creates a new function that, when the created function is called, has its `this` keyword set to a provided value.
It's most useful for binding the value of `this` in methods of classes you want to pass into other functions.

<div class="head">

## When would you use **document.write()**?

</div>

When you need to write to the **DOM/Document Object**, and essentially overwrite or clear the whole document, replacing it with the contents of `document.write()` (considered dangerous).


<div class="head">

## What's an **Immediately Invoked Function Expression**?

</div>

<div class="head">

## Explain **Ajax**

</div>

**Ajax** stands for **Asynchronous Javascript and XML**, and is a set of web development techniques using different client-side technologies to create asynchronous web applications.

Ajax lets you send and retrieve from a server without reloading the page or interfering with any behavior.

Ajax decouples the **data interchange** layer with the **presentation** layer.

Ajax takes advantage of `JSON` over `XML` because it's native to Javascript.

<div class="head">

## What are the advantages and disadvantages of **Ajax**?

</div>

#### Advantages

* Better `interactivity`
* **Reduce connection** to server since **scripts and services only have to be requested once**
* Advantages of **state being maintained on page**; Javascript variables and DOM state persist

#### Disadvantages

* Dynamic webpages are **harder to bookmark**
* Ajax doesn't work **if Javascript has been disabled in the browser**

<div class="head">

## What's **callback hell**?

</div>

<div class="head">

## What are some Javascript **anti-patterns**?

</div>

<div class="head">

## Have you ever used Javascript **templating**?

</div>

I've used **JSX** with React, and **Lodash**. JSX is very easy to learn since it's essentially HTML embedded in Javascript.

<div class="head">

## Explain **hoisting**

</div>

**Hoisting** is the idea that variables in a Javascript function are "hoisted" to the top of the scope, regardless of where they're called within the function.

However, **only the declaration is hoisted**, while the assignment, if there is one, stays where it is.

<div class="head">

## Explain **event bubbling**

</div>

When events of an element "bubble up" to the parent element. This occurs all the way up to the parent `document` object.

<div class="head">

## What's the difference between an **attribute** and a **property**?

</div>

Attributes are defined in the HTML markup, whereas properties are defined in the DOM.

<div class="head">

## Why is extending built-in JS objects not a good idea?

</div>

If you have multiple libraries that try to extend the `Array.prototype` object for example by adding the same `contains()` method, they will overwrite each other and the behavior will break.

<div class="head">

## What's the difference between document **load** and document **DOMContentLoaded** event?

</div>

`DOMContentLoaded` is an event that's fired when the initial HTML document has been completely loaded and parsed, without waiting for stylesheets or images to finish loading.

`window`'s `load` event is fired only after the DOM and all dependent resources and assets have loaded.

<div class="head">

## What is the difference between **==** and **===**?

</div>

**`==`** - the comparison operator, or **abstract** equality operator. <br/>
**`===`** - the strict comparison operator, or  **strict** equality operator.

**`==`** - does a comparison after performing necessary type conversions.
<br/>
**`===`** - **does not do type conversion**.

<div class="head">

## Explain the **same-origin policy** with regards to Javascript

</div>

The **same-origin policy** prevents JS from making requests across domain boundaries.
An **origin** is defined as **a combination of 1. URI scheme, 2. hostname, and 3. port number**.

This policy is used to prevent malicious scripts from obtaining access to sensitive data on another webpage through the **DOM**.

<div class="head">

## What does **ternary** mean in a ternary expression?

</div>

Ternary means three. A **ternary expressions** accepts three **operands**:

* The **test** condition,
* The **"then"** expression, and the
* **"else"** expression

<div class="head">

## What does **use strict** do?

</div>

Enables **strict mode**. Can be used on entire scripts or individual functions.

#### Advantages

* Makes it impossible to accidentally create global variables
* `this` is undefined in the global context

#### Disadvantages

* Many features are missing that developers might be used to

<div class="head">

## Explain what a single-page app is, and how to make one SEO-friendly

</div>

A single-page app takes advantage of **Ajax** and **state** to display an applications contents on the same page. Different elements are shown based on different user interactions.

Because **SPAs** rely on JS to render content, search engines may see empty content on the page. To overcome this, you can use a **server-side render**, or use a service such as **Prerender** to <br/> 1. Render JS in the browser, 2. Save static HTML, and 3. Return that to the crawlers.

<div class="head">

## What is the extent of your experience with **Promises**?

</div>

A Promise is an ***object*** that may produce a single value at some point in the feature: either resolved, or a reason that it's not resolved (i.e. a network error occurs). Promises have 3 states:

* Fulfilled
* Rejected
* Pending

<div class="head">

## What are the pros and cons of using **Promises** versus **callbacks**?

</div>

#### Pros

* Avoid **callback hell**, which can be unreadable

#### Cons

* Slightly more complex code
* In older browsers that don't support ES6 you need a polyfill to use it

<div class="head">

## Explain the difference between **mutable** and **immutable** objects

</div>

<div class="head">

## What are the differences between variables created using **let**, **var**, and **const**?

</div>

<div class="head">

## What's the difference between ES6 **classes** and ES5 function **constructors**?

</div>
[1014]

<div class="head">

## What's the advantage for using **arrow syntax** for a method in a constructor?

</div>

The value of `this` gets set at the time of function creation, and can't change after that. So, when the constructor creates a new object, `this` always refers to that object. [1067]

<div class="head">

## What's the definition of a **higher-order function**?

</div>

A **higher-order function** is any function that takes one or more functions as arguments, and/or returns a function as a result. They're meant to abstract an operation that's performed repeatedly. An example is `map`, which takes an array and a function as arguments.

<div class="head">

## Can you give an example for **destructuring** an object or an array?

</div>

**Destructuring** is an expression available as of ES6, and it enables a clear way to extract values of Objects or Arrays and place them into distinct variables.

Array destructuring:
```js
const foo = ['one', 'two', 'three'];

const [one, two, three] = foo;
console.log(one);
console.log(two);
console.log(three);
```

Object destructuring:
```js
const o = {  p: 42, q: true };
const { p, q } = o;
```

<div class="head">

## Can you give an example of **currying** and why this syntax offers an advantage?

</div>

**Currying** is a **pattern** where a function with more than one parameter is broken into multiple functions, each with a single parameter. When called in series, they'll accumulate all the required parameters one at a time. This helps when writing code in a more **functional** style so it's easier to read and compose.
[example wtf 1261]

<div class="head">

## How can you share code between files?

</div>

On the server **(Node)**, and **CommonJS** (**modules** - import-export).

<div class="head">

## Is there a difference between **window** and **document**?

</div>
 
JS has a **global object**, and `window` is in that global object with its own `Window Object`. `Document` is a property of the window object, and represents the **DOM**.

<div class="head">

## Why would you want to create **static class members**?

</div>

They're not tied to a specific instance of a class, and have the same value regardless of which instance is referring to it.

Static properties are typically configuration variables.
Static methods are usually pure utility functions which Don't depend on the state of the instance.

<div class="head">

## What's the **call stack**?

</div>

The call stack is a LIFO (Last in, First Out) queue.

<div class="head">

## What is the **event loop**?

</div>

It maintains a queue of tasks. It runs a continuous loop that waits synchronously for a task, runs it, and repeats.

1. JS maintains a queue of messages, which are essentially callbacks.

2. JS also maintains a call stack, which is a stack of frames for nested function calls that have not yet completed evaluating.

3. It runs a `while` loop that waits synchronously for a message, processes it synchronously, and repeats.

That while loop is literally something like:
```js
while (queue.waitForMsg()) {
    queue.processMsg();
}
```

JS code runs on a single thread - just one thing running at a time. This kind of limitation sounds bad but is actually helpful - it helps you simplify the program without having to worry about concurrency issues.

The event loop continuously checks the call stack to see if there's a function that needs to be run.

It adds any function call it finds to the call stack, and executes each one in order.

<div class="head">

## What formats can you used to write an **Ajax** request?

</div>

Ajax can be written in the following formats:

* Text file
* HTML
* JSON Object


<div class="head">

## What's the **Fetch API**?

</div>

The **Fetch API** was introduced in ES6 and you use JS to **fetch resources**.
It's a more feature-packed alternative to `XMLHttpRequest`. It uses **Promises**, and simplifies the process of fetching resources in JS.

Fetch provides **Request** and **Response** objects.



<div class="head">

## Can you explain **scope?** (**block** vs. **function**)

</div>

**Function scope** is a scope that's created when a function is created. It's anything inside the function, and it can also be nested.

**Block scope** is anything in-between brackets (**a block is delimited by curly brackets**).

Example of a block:

```js
if (something == true) {

}
```

<br/>`var` functions differently depending on where declared.

* A var declared in function scope can't be accessed outside of it:

```js
function haveScope() {
  var something = 42;
}
something; // ReferenceError: secret is not defined (in this scope)
```

* A var declared in block scope is available outside of that scope:

```js
for (var i=0; i<10; i++) {
  // block scope for the for statement
}
console.log(i) // => 10
```

<div class="head">

## What's **recursion**?

</div>

**Recursion** is when a function call itself repeatedly, until it arrives at a result. 
This is a technique for iterating over an operation.

<div class="head">

## What's the difference between **export** and **module.exports**?

</div>

* `module.exports` gets returned from `require()`. It's an empty object by default.

* `exports` is never returned; it's just a **reference to `module.exports`**, used to write less code.

<div class="head">

## Can you give a summary of **object-oriented programming**?

</div>

The basic concept of **OOP** is using objects to model real world things you would want in a program. Objects **encapsulate data**, they have **properties**, and usually expose **methods** you use to operate on these properties.

**Polymorphism** - Presenting the same interface for different forms (data types). The programmer doesn't have to know the exact type of an object, which is called dynamic binding.

**Abstraction** - Creating a simple model of real-world entities.

**Encapsulation** - When data can be stored inside an object "package" (which can be given a namespace). This is to make it easier to access.

**Inheritance** - In Javascript, objects inherit their features from their parent prototypes.

<div class="head">

## What are **arrow functions**?

</div>

**Arrow functions** were introduced in ES6, and are essentially anonymous functions with their own special syntax, and a more intuitive binding for `this`.

An example of when not to use an arrow function is in a dynamic context, because `this` doesn't work when bound dynamically in arrow functions.


<div class="head">

## Can you explain **form validation**?

</div>

You can use JS to do **HTML form validation**. For example you can create a **regex** to verify that a user inputs an email in the proper format, or a phone number.


<div class="head">

## What are the **primitive** and **non-primitive** data types?

</div>

There are 7 total data types.

**6** Primitive:

* **string**
* **number**
* **boolean**
* **null**
* **undefined**
* **symbol** (new in **ES6**)

**1** Non-primitive:

* **Object**

<div class="head">

## What's an **object literal**?

</div>

An **object literal** is a comma-separated list of key-value pairs in curly braces.
(Object literal = object)

<div class="head">

## Can you explain the **for…of** loop?

</div>

`for...of` was introduced in ES6. It's used to loop over iterable objects (Arrays, strings, Maps, Sets, etc.).

Syntax:

```js
for (variable of iterable) {
  statement
}
```

<div class="head">

## What are **Getters and Setters**?

</div>

**Getters** and **setters** are used to get (**Accessor**) and set (**Mutator**) the values of a variable.

<div class="head">

## Can you give a summary of **Big O Notation**?

</div>

<div class="head">

## Can you give an example of **O(1) (Constant)**?

</div>

Accessing an array index:

```js
var a = arr[5];
```

<div class="head">

## Can you give an example of **O(n) (Linear)**?

</div>

Linear search.

Also checking for a palindrome:

```js
function palindrome(str) {
  var lowRegStr = str.toLowerCase()
  var reverseStr = lowRegStr.split('').reverse().join(''); 
  return reverseStr === lowRegStr;
}

palindrome("a man, a plan, a canal. panama");
```

<div class="head">

## Can you give an example of **O(log n) (Logarithmic)**?

</div>

Binary search

<div class="head">

## Can you give an example of **O(n log n)**?

</div>

Merge sort; divide and conquer

<div class="head">

## Can you give an example of **O(n<sup>2</sup>) (Quadratic)**?

</div>

Bubble sort

<div class="head">

## Can you explain **dependency injection**?

</div>

**Dependency injection** is when an object supplies the dependencies of another object. The dependency itself is also an object, and can be used as a **service**.

<div class="head">

## Can you explain **functional programming**? 

</div>

**Functional Programming** is a programming paradigm where you treat computations as the evaluation of a mathematical expression, and **avoid changing state**, **mutable data**, and **side effects**.

<div class="head">

## Can you explain the concept of **MVC**?

**MVC** is an architectural pattern usually used when developing UIs. The application is divided into 3 parts:

1. The **model** represents the data
2. The **view** displays the model data (aka UI elements)
3. The **controller evaluates HTML expressions** . *The view, when interacted with, sends user actions to the controller*.

</div>

<div class="head">

## What are some **problems/limitations** with JS?

</div>

* It's not search engine friendly
* It can't access databases
* It depends largely on the browser
* It can be disabled
* Javascript doesn't allow the reading or writing of files for security reasons

<div class="head">

## What are the different ways of creating an object?

</div>

There are 3 main ways to create objects:

1. An **object literal** (ex: `var car = {something: else,…};`
2. **Constructors**
3. **Classes** (syntactical sugar over the already-existing prototypal inheritance)

There's also a fourth way, `Object.Create` method.

<div class="head">

## What's the difference between **public** versus **private** properties?

</div>

A **private function** can only be used inside of its parent function or module.

A **public function** can be used inside or outside of it.

Public functions can still call private functions inside them.

<div class="head">

## Can you explain **strong** versus **weak** typing?

</div>

**Strong** - Doesn't convert between data types implicitly

**Weak** - What Javascript uses: does do data type conversion

</div>

<div class="head">

## Can you explain **static** versus **dynamic** typing?

</div>

**Static** - Types are checked at **run-time**

**Dynamic** - Types are check on the fly, during execution

</div>

<div class="head">

## Can you explain **extends**?

</div>

It's used with JS classes to define a child of another preexisting class


<div class="head">

## What's an **expression** in JS?

</div>

**Expression** - any valid **unit of code that resolves to a value**
*
Javascript has the following expression categories:
* **Arithmetic**: evaluates to a number, for example 3.14159 (generally using arithmetic operators
* **String**: evaluates to a character string, for example "Bob"
* **Logical**: evaluates to a boolean value
* **Primary** expressions
* **Left-hand-side** expressions

# **jQuery Questions**

<div class="head">

## How is jQuery different from Javascript?

</div>

jQuery isn't a programming language, but a JS framework. It absracts cross-browser compatibility issues away, and emphasizes a more simplfied approach to callback-driven JS programming.

<div class="head">

## What does **$()** do in jQuery?

</div>

It's an alias of jQuery() function. It allows you to wrap any object into a jQuery object, which allows you to call the various methods defined in the jQuery object.

<div class="head">

## Implement a function that hides an image on button click using jQuery

</div>

```js

$("#button").click(function(){
	$("#image").hide();
});
```

<div class="head">

## What are some of the **event handlers** in jQuery?

</div>

* `bind()`
* `unbind()`
* `blur()`
* `hover()`
* `ready()`












