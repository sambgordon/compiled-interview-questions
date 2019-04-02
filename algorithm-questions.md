<style>.head{ color: #fcf101; }
.body{ color: #2491f2; font-weight: bold; }
</style>

# Algorithm Questions

<div class="head">
 
## Check for palindrome

  </div>

  ```js
  function palindrome(str) {
    var re = /[\W_]/g;
    var lowRegStr = str.toLowerCase().replace(re, '');
    var reverseStr = lowRegStr.split('').reverse().join(''); 
    return reverseStr === lowRegStr;
  }
  palindrome("A man, a plan, a canal. Panama");
  ```

<div class="head">
 
## Check for prime number

</div>

  ```js
  //A prime number is divisible only by itself and 1.
  //You can use a while loop and increase by 1.
  //If a number is divisible by any even number, it will be divisibly by 2.

  function isPrime(n){ //check if an in out n is prime
  var divisor = 2; //use to determine a number is prime or not by being divisible by 2

  while (n > divisor){ //as long as n is greater than 2,
    if(n % divisor == 0){//if n can be divided by 2, return false
      return false;
    } else
    divisor++; //else increment 
  }
  return true;
  }
  ``` 
<div class="head">
 
## Convert a date into a string explaining "time from now"

</div>

<div class="head">
 
## Diff two arrays

</div>

<div class="head">
 
## Factorialize
</div>

<div class="head">
 
## Find longest word in an array
</div>

<div class="head">
 
## Reverse a string

</div>

<div class="head">
 
## Reverse words in place

<div class="head">
 
## Word counter
</div>

<div class="head">
 
## Date format converter

</div>

Write a function that converts user-entered date, formatted as M/D/YYYY, to a format required by an API (YYYYMMDD).
<div class="head">
 
## Split string and convert to array of words

</div>

  ```js
  function splitted(str){
    str.split("");
  }
  ```
<div class="head">
 
## Extract specified number of characters from a string

</div>

  ```js
  function truncateString(str, length){ //length = number of chars to be extracted
    str.slice(0, length); //start at 0 index
}
  ```
<div class="head">
 
## Accept an array and return the last item in the array

</div>

  ```js
  function arrLast(arr){
    return arr.pop();
  }
  ```
<div class="head">
 
## Calculate the number of digits in a given number

</div>

  ```js
  function calc(num){
    var toCalc = numtoString();
    return  toCalc.length;
  }
  ```
<div class="head">
 
## Implement **registerClickHandler** function

</div>

Implement it so it registers a click event handler and implements the following logic: 
When the button of class remove is clicked, its parent &lt;`div`&gt; should be removed from the gallery:
  ```js
  function registerClickHandler(){
  getElementById('remove').addEventListener("click", function(){
    getElementById('remove).parentElement.innerHTML = "":
    });
  }
  function registerClickHandler(){
    var remove = getElementById('toRemove');

    toRemove.addEventListener("click", function(){
      toRemove.parentNode.removeChild(toRemove);
    });
  }
  ```
<div class="head">
 
## Evaluate whether an input is truthy or falsy

</div>

  ```js
  function isTruthy(input){
    if(input){
    return 1;
    } else {
    return 0;	
    }
  }
  ```
<div class="head">
 
## Find smallest number in array

</div>

  ```js
  const findSmallestNum = (arr) => {
    return Math.min(…arr);
  }
  ```

<div class="head">
 
## Hurdle Height

</div>

<div class="body">
  Create a function that takes an array of hurdle heights and a jumper's jump height and determines whether or not the hurdler can clear all the hurdles. A hurdler can clear a hurdle if their jump height is greater than or equal to the hurdle height.
</div>

  ```js
  function hurdleJump(hurdles, jumpHeight) {
    if (jumpHeight >= Math.max(...hurdles)){
      return true;
    } else if (hurdles.length == 0){
      return true;
    } else return false;
  }
  ```
<div class="head">
 
## Give an example of an algorithm with constant O(1) complexity

</div>

#### Accessing an array index:
  ```js
  var a = arr[2];
  ```
<div class="head">
 
## Give an example of an algorithm with linear O(n) complexity

</div>

<div class="head">
 
#### Check for palindrome:

</div>

  ```js
  function checkPalindrome(str) {
    var reversed = str.split("").reverse().join("");
    if (str == reversed) {
      return "is palindrome";
    } else {
      return "isn't palindrome";
      }
  }

  checkPalindrome("hello"); //returns isn't palindrome
  ```
<div class="head">
 
## Give an example of an algorithm with logarithmic O(log n) complexity
<div class="head">
 
#### Fibonacci (golden ratio):

</div>

  ```js
  function fibonacci(num){
    for (i = 0; i < 100; i++) {
      return fibonacci (num - 1) + fibonacci (n - 2);
    } ~~
  }

  //FIBONACCI IS RECURSIVE SO IT HAS TO CALL ITSELF
  ```
<div class="head">
 
## How would you verify if one element is a child of another?

</div>

  ```js
  const isDescendant = (parent, child) => {
    if(child.parentNode == parent) {
    return true
    } else {
      child = child.parentNode
    };
  }
  ```
<div class="head">
 
## Capitalize first letter of each word in string

</div>

  ```js
  var capitalize = (str) => {
    var splitted = str.split("").charAt[0].toUpperCase() +
    str.slice(1);
    var joined = splitted.join("");
  };
  ```
<div class="head">
 
## Extract specified number of characters from string

</div>

  ```js
  var truncateString = (str, length) => { //string AND specified length need to be params
  str.slice(0, length); //start at zero index, then specify number
  };
  truncateString("Billy Bob", 4);
  ```
<div class="head">
 
## Find all even numbers from 1 to the given number

</div>

  ```js
  const findEvenNums = num => {
  var val;
  while (1 < val < num) {
  if (num % 2 == 0) {
  return val;
  } else return [];
  }
  };
  ```

<div class="head">
 
## Take in 3 parameters and determines whether or not a gamble is profitable

</div>

  ```js
  //1. Probability of winning
  //2. Prize value
  //3. Cost of playing
  //and returns whether or not the gamble is profitable.
  //A profitable gamble will be a game that yields a positive net profit; net profit is calculated as: 
  //net_outcome = probability_of_winning * prize_value - cost_of_playing

  const profitableGamble = (prob, prize, pay) => {
  var net_outcome = prob * prize - pay;
  if (net_outcome > 0) {
  return true;
  } else {
  return false;
  }
  };
```

<div class="head">
 
## Determine and classify missing angle as "acute", "right", or "obtuse"
</div>

```js
            // //An acute angle is smaller than 90 degrees.
            // //A right angle is 90 degrees.
            // //An obtuse angle is greater than 90 but smaller than 180.

            function missingAngle(angle1, angle2) {
              if (180 - angle1 - angle2 < 90) {
                return "acute";
              } else if (180 - angle1 - angle2 == 90) {
                return "right";
              } else if (180 - angle1 - angle2 > 90 && 180 - angle1 - angle2 < 180) {
                return "obtuse";
              }
            }
```

<div class="head">
 
## Sum two numbers and return sum using Javascript on elements
</div>

  ```html
  <input id="numOne"> + <input id="numTwo">
  <div id="sum"></div>
  ```
  ```js
  var numOne = document.getElementById("numOne");
  var numTwo = document.getElementById("numTwo");
  var sum = document.getElementById("sum");

  numOne.addEventListener("input", addNumbers);
  numTwo.addEventListener("input", addNumbers);

  function addNumbers(){
      var one = parseFloat(numOne.value) || 0;
      var two = parseFloat(numTwo.value) || 0;
      sum.innerHTML = one + two;
  };

  //1. Create the numbers to be added as inputs with corresponding id's; create element to be updated with the returned sum
  //2. Define the elements to be used in JS using document.getElementById
  //3. Add event listeners to the elements, a. listening for the input type and b. executing function addNumbers when input being watched or listened to is changed
  //4. Create function addNumbers, that stores numOne and numTwo in corresponding vars - params are empty since already instantiated outside of function
  //5. Parse the string value of numOne and numTwo; add or exception so "NaN" is replaced by 0 - so empty input doesn't return NaN.
  //6. Use innerHTML to update sum's contents with the new added total.
  ```

<div class="head">
 
## Sum two numbers and output the result
</div>

  ```html
  <input id="numOne"> + <input id="numTwo">
  <div id="sum"></div>
  ```
  ```js
  var numOne = document.getElementById("numOne");
  var numTwo= document.getElementById("numTwo");

  numOne.addEventListener("input", add);
  numTwo.addEventListener("input", add);

  function add(){
    var output = parseFloat(numOne.value) + parseFloat(numTwo.value);
    sum.innerHTML = output; //target sum, update innerHTML with output's contents
  });
  ```
<div class="head">
 
## Make this work:

</div>

  ```js
  duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```

<div class="head">
 
## fizzbuzz

</div>

* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`

<br/>

# More Exercises

### What's the value of `foo`?
```javascript
var foo = 10 + '20';
```

###  What will be the output of the code below?
```javascript
console.log(0.1 + 0.2 == 0.3);
```

### How would you make this work?
```javascript
add(2, 5); // 7
add(2)(5); // 7
```

### What value is returned from the following statement?
```javascript
"i'm a lasagna hog".split("").reverse().join("");
```

### What is the value of `window.foo`?
```javascript
( window.foo || ( window.foo = "bar" ) );
```

### What is the outcome of the two alerts below?
```javascript
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

### What is the value of `foo.length`?
```javascript
var foo = [];
foo.push(1);
foo.push(2);
```

### What is the value of `foo.x`?
```javascript
var foo = {n: 1};
var bar = foo;
foo.x = foo = {n: 2};
```

### What does the following code print?
```javascript
console.log('one');
setTimeout(function() {
  console.log('two');
}, 0);
Promise.resolve().then(function() {
  console.log('three');
})
console.log('four');
```

### What is the difference between these four promises?
```javascript
doSomething().then(function () {
  return doSomethingElse();
});

doSomething().then(function () {
  doSomethingElse();
});

doSomething().then(doSomethingElse());

doSomething().then(doSomethingElse);
```
