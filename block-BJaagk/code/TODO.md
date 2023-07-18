1. Convert the function below into different forms of function expression.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}

// Your code goes here

//Arrow Function
const percentage = (marks, total) => (marks * 100) / total;

//Function Expression
const percentage = function(marks, total) {
  return (marks * 100) / total;
};

//Shorthand Function Expression

const percentage = function percent(marks, total) {
  return (marks * 100) / total;
};

//IIFE (Immediately Invoked Function Expression)

(function(marks, total) {
  return (marks * 100) / total;
})(marks, total);

```

2. Write Function Declaration or Function Expression next to the function.

```js
function percentage(marks, total) {
  return (marks * 100) / total;
}
// Your answer
```
// fxn expresion
let percentage = function(marks, total) {
  return (marks * 100) / total;
};

```js
let percentage = function percentage(marks, total) {
  return (marks * 100) / total;
};
```
// fxn declaration
function percentage(marks, total) {
  return (marks * 100) / total;
}

```js
let percentage = function (marks, total) {
  return (marks * 100) / total;
};
```

// fxn declaration
function percentage(marks, total) {
  return (marks * 100) / total;
}

```js
let percentage = (marks, total) => {
  return (marks * 100) / total;
};
```

// fxn declaration
function percentage(marks, total) {
  return (marks * 100) / total;
}

```js
let percentage = (marks, total) => (marks * 100) / total;

// fxn expression

let percentage = function(marks, total) {
  return (marks * 100) / total;
};

// fxn declaration
function percentage(marks, total) {
  return (marks * 100) / total;
}

```

3. Why is a function definition an expression in JavaScript? Give one example of function expression.

In JavaScript, a function definition is considered an expression because it can be assigned to a variable, passed as an argument to another function, or used in other expressions

```js
let addNumbers = function(a, b) {
  return a + b;
};

```
4. Why is a function call an expression in JavaScript?

In JavaScript, a function call is considered an expression because it evaluates to a value. When a function is called, it executes the code inside the function body and returns a result

```js

let addNumbers = function(a, b) {
  return a + b;
};

let result = addNumbers(5, 3);

```


5. Write VALID and INVALID next to each example below with the reason.

```js
function add(a, b) {
  return a + b;
}

let five = add(2, 3); //{valid} This is a valid function call. The add function is called with the arguments 2 and 3, and the returned value is assigned to the variable five.

five = add; // {valid} This is valid because it assigns the function reference to the variable five. Now five holds a reference to the add function.

five = five(10, 11); // {invalid} This is invalid because the variable five was previously assigned a function reference, but in this line, it is being called as a function. However, five is not a function at this point, so it will result in a TypeError.


five = function () {
  return 'Hello';
}; // {valid} This is valid because it assigns an anonymous function to the variable five. The function can be invoked later using five().
```

6. What is the difference between function definition and function call? Explain with an example.
// Function Definition:
A function definition is the actual creation of a function that defines its behavior and structure.
It involves specifying the function name, parameter list, and the code that will be executed when the function is called.
Function definitions are used to define reusable blocks of code that can be invoked later.
They are typically written once and can be called multiple times throughout the program.

```js
function greet(name) {
  console.log("Hello, " + name + "!");
}
```
//Function Call (or Invocation):

A function call is the execution or use of a previously defined function.
It involves invoking the function using its name, along with providing any required arguments.
Function calls allow the code to execute the statements within the function's body and potentially return a value.
Function calls are used to use the functionality provided by the defined function at a specific point in the program.

```js
greet("Arya Stark");
```
7. What is the similarities between function definition and function call?
//
1.Both involve the use of parentheses:

Function definitions use parentheses to enclose the parameter list.
Function calls use parentheses to enclose the arguments being passed to the function.
```js
// Function Definition
function greet(name) {
  console.log("Hello, " + name + "!");
}

// Function Call
greet("Arya");

```
//2. Both are essential components of using functions:

Function definitions are necessary to define the behavior and structure of a function.
Function calls are essential to invoke the defined function and execute its code.

```js
// Function Definition
function greet(name) {
  console.log("Hello, " + name + "!");
}

// Function Call
greet("Alice");

```
//3.Both can have side effects or return values:

Function definitions specify the code that will be executed when the function is called and can have side effects (such as console output) or return a value.
Function calls execute the code within the function's body and can also have side effects or capture the returned value.
```js
// Function Definition
function multiply(a, b) {
  return a * b;
}

// Function Call with Side Effect
console.log(multiply(2, 3)); // Output: 6

// Function Call with Value Assignment
let result = multiply(4, 5);
console.log(result); // Output: 20

```
8. Is the code below valid or invalid. Explain with reason.

```js
function hello() {
  console.log('Hello World!');
}

hello.user = 'Sam'; // valid 
```
// The code hello.user = 'Sam'; is valid in JavaScript.

In JavaScript, functions are objects, and as objects, they can have properties assigned to them. In the given code, the hello function is defined using a function declaration, and afterward, the property user is assigned the value 'Sam' to the hello function object.

This code snippet assigns a property user with the value 'Sam' to the hello function object. The function object now has an additional property user with the value 'Sam'. This can be useful in certain scenarios, such as attaching metadata or additional information to the function object.

The code will not produce an error and is considered valid JavaScript. However, it's important to note that adding properties to a function object should be used judiciously, as it can make the code less clear and may have unintended consequences.

9. What is higher order function explain with an example.
// In JavaScript, a higher-order function is a function that either takes one or more functions as arguments or returns a function as its result. In other words, it operates on functions, treating them as values and allowing them to be manipulated or used in different ways.

```js
function operationLogger(operation, a, b) {
  console.log("Performing operation: " + operation.name);
  const result = operation(a, b);
  console.log("Result: " + result);
}

function add(a, b) {
  return a + b;
}

function subtract(a, b) {
  return a - b;
}

operationLogger(add, 5, 3);
operationLogger(subtract, 10, 4);

```
10. Explain what is callback function. Why you can pass a function inside a function?
// In JavaScript, a callback function is a function that is passed as an argument to another function and is later invoked within that function. The callback function is typically used to specify what should happen once a certain task or operation is completed.

```js
function calculate(num1, num2, operationCallback) {
  const result = operationCallback(num1, num2);
  console.log("The result is: " + result);
}

function add(a, b) {
  return a + b;
}

calculate(5, 3, add);

```