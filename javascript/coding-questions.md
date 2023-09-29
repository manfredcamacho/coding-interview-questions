## 1. Consider following code snippet:

<dl>
<dd>

```javascript
function A (){...}
function B (){...}
var a = new A()
var b = new B()

console.log( a == b) //true

```

Select the correct option if is it possible to create two new Ojects `a` and `b` that will return the true on comparing them `(a == b)`?

<br/>
<dd>
Option A

```javascript
function A() {return arr;}
function B() {return arr;}
var arr[];
var a = new A;
var b = new B;
```

Option B

```javascript
function A() {
  return this;
}
function B() {
  return this;
}
var a = new A();
var b = new B();
```

Option C

```javascript
function A() {
  return {};
}
function B() {
  return {};
}
var a = new A();
var b = new B();
```

Option D

```
None of the above
```

</dd>

<br/>

<details>
<summary>Answer</summary>

```
None of the above
```

Non-primitive data types are compared by reference in JavaScript. When you create a new object using the `new` keyword, a new reference is created. As a result, the objects will never be equal.

</details>

</dd>
</dl>

<br/>

## 2. What is the output of the following JS snippet code?

<dl>
<dd>

```javascript
var sam = function () {
  console.log("hello");
};

console.log(sam() === undefined);
```

<br/>
<dd>
Option A

```
hello
true
```

Option B

```
hello
false
```

Option C

```
error
```

Option D

```
hello
```

</dd>

<br/>

<details>
<summary>Answer</summary>

```
hello
true
```

The function `sam` is called and print `hello` on the console. Since the function doesn't return anything explicitly, it returns `undefined` by default.

</details>

</dd>
</dl>

<br/>

## 3. What is the output of the following JS snippet code?

<dl>
<dd>

```javascript
function sum(a, b) {
  return a + b;
}

console.log(sum(1, 2, 3, 4));
```

<br/>
<dd>
Option A

```
Error: arguments does not match
```

Option B

```
3
```

Option C

```
10
```

Option D

```
None
```

</dd>

<br/>

<details>
<summary>Answer</summary>

```
3
```

The function `sum` takes only two arguments. The extra arguments are ignored.

</details>

</dd>
</dl>

<br/>

## 4. What does the following code print to the console?

<dl>
<dd>

```javascript
var happy = {
  hi: function sing(n, result) {
    result = typeof result !== "undefined" ? result : [];
    if (n == 0) {
      result.push("No more bottles");
      return result;
    }
    var str = n + " bottles";
    result.push(str);
    return sing(n - 1, result);
  },
};

console.log(happy.hi(3));
```

<br/>
<dd>
Option A

```
3 bottles
```

Option B

```
No more bottles

```

Option C

```
3 bottles, 2 bottles, 1 bottles, No more bottles
```

Option D

```
None
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
3 bottles, 2 bottles, 1 bottles, No more bottles
```

The function `sing` is a recursive function that prints the lyrics of the song "99 bottles of beer". The function `sing` takes two arguments, `n` and `result`. The argument `n` is the number of bottles of beer. The argument `result` is an array that stores the lyrics of the song. The function `sing` returns the array `result` when `n` is equal to `0`.

</details>

</dd>
</dl>

<br/>

## 5. What is the output of the following JS snippet code?

<dl>
<dd>

```javascript
var sample = {
  x: "y",
  func: function () {
    var self = this;
    console.log("outer func: " + this.x);
    console.log("outer func: " + self.x);
    (function () {
      console.log("inner func: " + this.x);
      console.log("inner func: " + self.x);
    })();
  },
};
sample.func();
```

<br/>
<dd>
Option A

```
outer: y
outer: y
inner: undefined
inner: y
```

Option B

```
outer: y
outer: y
inner: undefined
inner: undefined
```

Option C

```
outer: y
outer: undefined
inner: undefined
inner: y
```

Option D

```
Error due to self
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
outer: y
outer: y
inner: undefined
inner: y
```

The `this` keyword refers to the object that the function is a property of. Inside of anonymous function `this` is always the global object, or `undefined` in `strict mode`. Since the global object has no `x` property, `this.x` is `undefined`.

</details>

</dd>
</dl>

<br/>

## 6. What will be printed to the console?

<dl>
<dd>

```javascript
for (var i = 0; i < 10; i++) {
  setTimeout(function () {
    console.log(i);
  }, 0);
}
```

<br/>
<dd>
Option A

```
0,1,2,3,4,5,6,7,8,9
```

Option B

```
10 times the number 10 will be printed
```

Option C

```
10
```

Option D

```
Error
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
10 times the number 10 will be printed
```

The reason for this is that the variable `i` is declared using the `var` keyword. And the scope of the variable `i` is global. So when the `setTimeout` callback function is invoked, it prints the value of the global variable `i`, which at the end of the loop is equal to `10`.

</details>

</dd>
</dl>

<br/>

## 7. What will be printed to the console?

<dl>
<dd>

```javascript
phone = {
  ring: function () {
    return this === phone;
  },
};

console.log(phone.ring());
```

<br/>
<dd>
Option A

```
true
```

Option B

```
false
```

Option C

```
1
```

Option D

```
0
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
true
```

The `this` keyword refers to the object that the function is a property of. So, `this` refers to the object `phone` and the expression `this === phone` returns `true`.

</details>

</dd>
</dl>

<br/>

## 8. What will be the output?

```javascript
var num = 1;

if (1) {
  eval(function foo() {});
  num += typeof foo;
}

console.log(num);
```

Option A

```
1undefined
```

Option B

```
1
```

Option C

```
1+undefined
```

Option D

```
undefined
```

<details><summary>Answer</summary>

```
1undefined
```

`eval()` has a Block Scope, variables declared inside a { } block cannot be accessed from outside the block.

</details>
<br/>

## 9. What is the difference between the following two in javascript?

<dl>
<dd>

```javascript
var myString = new String("male");
var myStringLiteral = "male";
```

<br/>
<dd>
Option A

```
Both are primitive strings
```

Option B

```
Both are objects
```

Option C

```
First one is object, second is primitive string
```

Option D

```
First one is primitive string, second is object
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
First one is object, second is primitive string
```

The first one is an object created with the `String` constructor. The second one is a primitive string.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 10. which one of the following error(s) is not shown in JavaScript?

<dl>
<dd>

<br/>
<dd>
Option A

```
Run-time error
```

Option B

```
Compilation error
```

Option C

```
Load-time errors
```

Option D

```
Logic error
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
Compilation error
```

JavaScript is an interpreted language, which means it doesn't go through a separate compilation step before execution. Instead, it is interpreted line by line as it is executed.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 11. Which of the following statements are true in case of Javascript?

<dl>
<dd>

<br/>
<dd>
Option A

```
Javascript can react to events
```

Option B

```
Javascript can create cookies
```

Option C

```
Javascript can read and write HTML elements
```

Option D

```
All
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option D

```
All
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 12. Which is a Javascript running in the background, without affecting the performance of the page?

<dl>
<dd>

<br/>
<dd>
Option A

```
Web Worker
```

Option B

```
Canvas
```

Option C

```
SVG
```

Option D

```
None of the above
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
Web Worker
```

Web Worker is a JavaScript feature that allows you to run scripts in the background without affecting the performance of the page. Web Workers enable multi-threading in JavaScript by executing scripts in separate background threads, allowing for tasks that are computationally intensive or time-consuming to run without blocking the main thread. This helps in keeping the user interface responsive while performing complex operations.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 13. The \_\_\_ returns true only if the named property is an own property and its enumerable attribute is true.

<dl>
<dd>

<br/>
<dd>
Option A

```javascript
hasOwnProperty();
```

Option B

```javascript
propertyIsEnumerable();
```

Option C

```javascript
getOwnProperty();
```

Option D

```javascript
isPrototypeOf();
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
propertyIsEnumerable()
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 14. With the following HTML and Javascript, the alert isn't shown when you click the button, why not?

<dl>
<dd>

```html
<input type="button" value="ClickMe" onClick="handleClick" />
<script>
  (function setup() {
    function handleClick() {
      alert("Clicked!");
    }
  })();
</script>
```

<br/>
<dd>
Option A

```
handleClick should be a global function
```

Option B

```
There should be () after handleClick in the onClick attribute
```

Option C

```
The setup function never runs
```

Option D

```
The setup function runs before the DOM is ready
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
handleClick should be a global function
```

The handleClick function is defined within the immediately invoked function expression (IIFE) setup(). Therefore, it is only accessible within the scope of that function and is not a global function.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 15. The purpose of \_\_ attribute is to be able to "lock down" objects into known state and prevent outside tempering.

<dl>
<dd>

<br/>
<dd>
Option A

```
prototype
```

Option B

```
class
```

Option C

```
extensible
```

Option D

```
literal
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
extensible
```

In JavaScript, the extensible attribute is used to determine if an object can have new properties added to it or if it is "extensible." By default, objects in JavaScript are extensible, meaning that new properties can be added to them. However, by setting the extensible attribute to false using the Object.preventExtensions() method, you can prevent any new properties from being added to the object.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 16. Which of the following Javascript conditions are true?

<dl>
<dd>

<br/>
<dd>
Option A

```
false === 0
```

Option B

```
false === ''
```

Option C

```
'abc' == 'abc'
```

Option D

```
false == 0
```

Option E

```
'1' === 1
```

Option F

```
'1' == 1
```

Option G

```
[1,2,3] == [1,2,3]
```

Option H

```
false == ''
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Options C, D, G, I

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 17. What will this Javascript code output?

<dl>
<dd>

```javascript
console.log(typeof a);
console.log(typeof b);

function a() {}

var b = function () {};
```

<br/>
<dd>
Option A

```
function, undefined
```

Option B

```
An error
```

Option C

```
undefined, undefined
```

Option D

```
function, function
```

Option E

```
undefined, function
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A

```
function, undefined
```

Hoisting is JavaScript's default behavior of moving all declarations (NOT initializations) to the top of the current scope, to the top of the current script or the current function.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 18. In JSON, which of the following is/are not allowed ?

<dl>
<dd>

<br/>
<dd>
Option A

```
functions or variables that involve computation
```

Option B

```
comments
```

Option C

```
global variables
```

Option D

```
none of the above
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option A, B, C

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 19. What will this javascript code output?

<dl>
<dd>

```javascript
var funcs = [];

for (var i = 0; i < 10; i++) {
  funcs.push(function () {
    console.log(i);
  });
}

funcs.forEach(function (func) {
  func();
});
```

<br/>
<dd>
Option A

```
Outputs 0, then 1, then 2, up to 9
```

Option B

```
Outputs undefined 10 times
```

Option C

```
Outputs the number 10 ten times
```

Option D

```
The code throws an error
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
Outputs the number 10 ten times
```

The variable `i` is declared using the `var` keyword. And the scope of the variable `i` is global. So when the `forEach` callback function is invoked, it prints the value of the global variable `i`, which at the end of the loop is equal to `10`.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 20. Given this declaration, Which of the following statements could be use to change the model attribute:

<dl>
<dd>

```javascript
const car = {
  model: "Audi",
};
```

<br/>
<dd>
Option A

```javascript
car = {
  model: "Mercedez Benz",
};
```

Option B

```javascript
car.model = "Mercedez Benz";
```

Option C

```
Both options (a and b) are correct
```

Option D

```
car is defined as a constant, therefore the model property can't be changed
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```javascript
car.model = "Mercedez Benz";
```

Since the car object is declared using the `const` keyword, the variable `car` cannot be reassigned. However, the properties of the object can be changed.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 21. What will this javascript code output?

<dl>
<dd>

```javascript
let promise = new Promise(function (resolve, reject) {
  console.log("Promise");
  resolve();
});

promise.then(function () {
  console.log("Resolved");
});

console.log("Hi!");
```

<br/>
<dd>
Option A

```
Resolved
Promise
Hi!
```

Option B

```
Promise
Resolved
Hi!
```

Option C

```
Hi!
Promise
Resolved
```

Option D

```
Promise
Hi!
Resolved
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option D

```
Promise
Hi!
Resolved
```

The order of execution is as follows:

- First, the promise’s executor function runs synchronously when the promise is created. In this case, the executor function logs `Promise` to the console.

- Each call to .then() adds a job to the queue (Jobs are run in the order they are enqueued). However, these jobs only run after the script finishes, which is why `Hi!` gets logged before `Resolved`.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 22. Having the following statements, Which of the following is true about importing modules in Javascript?

<dl>
<dd>

```javascript
import { sum } from "./operations.js";
import { multiply } from "./operations.js";
import { subtract } from "./operations.js";
```

<br/>
<dd>
Option A

```
The module will be executed on every import.
```

Option B

```
The module will be executed only once.
```

Option C

```
The module will be executed every time one of the sum, multiply or subtract functions is called.
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
The module will be executed only once.
```

The module is cached after the first execution, and the same module object is returned for every import thereafter.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 23. Suppose that you have a module example.js What would be the outp of the following code?

<dl>
<dd>

<i>example.js</i>

```javascript
export count = 5;
```

<br />

```javascript
import { count } from "./example.js";
count = 0;
console.log(count);
```

<br/>
<dd>
Option A

```
5
```

Option B

```
0
```

Option C

```
An Exception is thrown
```

Option D

```
Undefinded
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
An Exception is thrown
```

The importing module can only read the value but can't re-assign it.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 24. What would be the output of the following code?

<dl>
<dd>

```javascript
var count = 20;
let count = 30;
console.log(count);
```

<br/>
<dd>
Option A

```
20
```

Option B

```
30
```

Option C

```
The code throws an error
```

Option D

```
Undefined
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
The code throws an error
```

With `let` the variable `count` cannot be declared twice in the same scope.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 25. Is the next declaration of a derived class correct?

<dl>
<dd>

```javascript
class Square extends Rectangle {
  constructor(length)
  this.length = length;
}
```

<br/>
<dd>
Option A

```
Yes
```

Option B

```
No
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
No
```

The constructor of the derived class must call the constructor of the base class using the `super` keyword.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 26. Having the following declaration of Promises Which of the following statements is TRUE?

<dl>
<dd>

```javascript
let promise1 = Promise.resolve(123);

let promise2 = new Promise(function (resolve, reject) {
  resolve("abc");
});
```

<br/>
<dd>
Option A

```
The promise1 declaration throws an error.
```

Option B

```
Both declarations mwan exactly the same
```

Option C

```
The promise1 declaration creates a fulfilled promise, while the promise2 declaration schedules a job to be added to the javascript engine's job queue for future execution.
```

Option D

```
Both declarations schedule jobs to be added to the javascript engine's job quequed for future execution.
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option C

```
The promise1 declaration creates a fulfilled promise, while the promise2 declaration schedules a job to be added to the javascript engine's job queue for future execution.
```

The `Promise.resolve()` method returns a Promise object that is resolved with a given value. The `Promise.resolve()` method is useful if you already have a value, or if you want to create a resolved promise from an existing value.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 27. Which of the following is TRUE about the Promise.race()?

<dl>

<dd>
Option A

```
The method waits for all the promises to resolve and returns the array of promise results. If any of the promises reject or execute to fail due to an error, all other promise results will be ignored.
```

Option B

```
The method returns a promise that fulfills or rejects as soon as one of the promises in an iterable array is fulfilled or rejected. This array of promises is passed as an argument to the method.
```

Option C

```
There's no Promise.race() method
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option B

```
The method returns a promise that fulfills or rejects as soon as one of the promises in an iterable array is fulfilled or rejected. This array of promises is passed as an argument to the method.
```

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->

## 28. In a REST API that follows standards where would you find the pagination information (such as Next, Previous, First, Last)?

<dl>

<dd>
Option A

```
The pagination information should be returned in a separate request to a pagination endpoint.
```

Option B

```
In the body of the response. It should include a pagination attribute.
```

Option C

```
In the body of the response. It should include a metadata attribute containing the pagination information.
```

Option D

```
In the link header of the response.
```

</dd>

<br/>

<details>
<summary>Answer</summary>

Option D

```
In the link header of the response.
```

The link header is a response header that contains a set of hyperlinks that describe relationships between the response and some other resources.

</details>

</dd>
</dl>

<br/>

<!------------------------------------------------------->
