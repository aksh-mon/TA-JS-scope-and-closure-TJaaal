For the given code below:

- re-write the code in ways that system will understand

For Example:

1.

```js
var username = 'Arya';
let brothers = ['John', 'Ryan', 'Bran'];

console.log(username, brothers[0]);

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Declaration Phase
var username = undefined;
let brothers;

function sayHello(name) {
  return `Hello ${name}`;
}

let message;
var nextMessage = undefined;

// Execution Phase

username = 'Arya';
brothers = ['John', 'Ryan', 'Bran'];

console.log(username, brothers[0]);

message = sayHello(username);
nextMessage = sayHello('Test');
```

2.

```js
console.log(username, numbers);

var username = 'Arya';
let number = 21;

function sayHello(name) {
  return `Hello ${name}`;
}

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Your code goes here

// Declaration Phase

var username = undefined;

let number;

function sayHello(name) {
  return `Hello ${name}`;
}

let message;

var nextMessage = undefined;

// Execution Phase

console.log(username, numbers); 

username = 'Arya';
number = 21;

message = sayHello(username);
nextMessage = sayHello('Test');

```

3.

```js
console.log(username, numbers);
let username = 'Arya';
let number = 21;

let sayHello = function (name) {
  return `Hello ${name}`;
};

let message = sayHello(username);
var nextMessage = sayHello('Test');
```

<!-- Answer -->

```js
// Your code goes here
// Declaration Phase
let username; 
let number; 
let sayHello; 
let message; 
var nextMessage = undefined; 

// Execution Phase

console.log(username, numbers); // 'username' is undefined, 'numbers' is not defined

let username = 'Arya';
let number = 21; 

let sayHello = function (name) {
  return `Hello ${name}`;
}; 

let message = sayHello(username); 
var nextMessage = sayHello('Test'); 

```

4.

```js
let username = 'Arya';
console.log(username, numbers);

let number = 21;
let message = sayHello(username);

let sayHello = function (name) {
  return `Hello ${name}`;
};

var nextMessage = sayHello('Test');
```
<!-- Answer -->

```js

// Your code goes here

// Dec:

let username;
let number;
let message;
let sayHello;
var nextMessage = undefined;

// Exe :

username = 'Arya';
console.log(username, numbers); // Output: "Arya undefined" (numbers is not defined)

number = 21;

sayHello = function (name) {
  return `Hello ${name}`;
};

message = sayHello(username);

nextMessage = sayHello('Test');
```

5.

```js
console.log(name);
console.log(age);
var name = 'Lydia';
let age = 21;
```

<!-- Answer -->

```js
// Your code goes here

// Dec
var name;
let age;

// Exe

console.log(name); 
console.log(age); 

name = 'Lydia';
age = 21;

```

6.

```js
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}

sayHi();
```

<!-- Answer -->

```js
// Your code goes here

// Dec

sayHi = fn

// Exe

function sayHi(name) {
  var name;
  let age; 

  console.log(name); 
  console.log(age); 

  name = 'Lydia'; 
  let age = 21; 

}

sayHi(); // Function call with no arguments.

```

7.

```js
sayHi();
function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}
```

<!-- Answer -->

```js

// Your code goes here

// Dec

var name;
let age;

// Exe

console.log(name); 

console.log(age); 

name = 'Lydia'; 

age = 21; 
 
```

8.

```js
sayHi();
let sayHi = function sayHi(name) {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
};

```

<!-- Answer -->

```js
// Your code goes here

// Dec

let sayHi; 

// Execution Phase
sayHi(); 

sayHi = function sayHi(name) {

  var name; 
  let age; 

  // Exe sayHi() Function Context
  console.log(name); // Output: undefined (the variable 'name' is declared but not yet initialized)
  console.log(age); // Output: undefined (the variable 'age' is declared but not yet initialized)

  name = 'Lydia';
  let age = 21; 
  };

```

9.

```js
let num1 = 21;
console.log(sum);
var sum = num1 + num2;
let num2 = 30;
```

<!-- Answer -->

```js
// Your code goes here

// Dec
let num1;
var sum = undefined;
let num2;

// Exe
num1 = 21; 

console.log(sum); // Output: undefined (sum is hoisted and initialized with undefined)

sum = num1 + num2; 

num2 = 30; // Variable assignment for 'num2'

```

10.

```js
var num1 = 21;

let sum2 = addAgain(num1, num2, 4, 5, 6);

let add = (a, b, c, d, e) => {
  return a + b + c + d + e;
};
function addAgian(a, b) {
  return a + b;
}
let num2 = 200;

let sum = add(num1, num2, 4, 5, 6);

```

<!-- Answer -->

```js
// Your code goes here

// Dec

var num1 = undefined;
let sum2;
let add;
addAgain = fn;
let num2;
let sum;

// Execution Phase
num1 = 21; 

sum2 = addAgain(num1, num2, 4, 5, 6); 

add = (a, b, c, d, e) => {
  return a + b + c + d + e;
}; 

let num2 = 200; 

sum = add(num1, num2, 4, 5, 6); 

```

11.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

let add = (a, b) => {
  return a + b;
};
```

<!-- Answer -->

```js
// Your code goes here

// Dec
test = fn;
let sum;
let add;

// Exe

add = (a, b) => {
  return a + b;
}; 

let num1; 

sum = test(100);

function test(a) {
  num1 = 21; 
  return add(a, num1); 
}

```

12.

```js
function test(a) {
  let num1 = 21;
  return add(a, num1);
}

let sum = test(100);

function add(a, b) {
  return a + b;
}
```

<!-- Answer -->

```js
// Your code goes here

// Dec
test = fn;

let sum;

add = fn;

// Exe

function test(a) {
  let num1 = 21;
  return add(a, num1);
}

function add(a, b) {
  return a + b;
}
sum = test(100); // Function call after declaration

```
