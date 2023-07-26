Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

Example:

```js
function hello() {
  var username = 'Arya';
}
console.log(useranme); // output
```

In above code we are looking for the variable named `usename`. There is no variable named `username` in the global scope. The variable is inside the function named `hello` and we can't access the variable defined inside a function from outside.

The above code will throw an error `Reference Error username is not defined`.

2. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
{
  const username = 'Arya';
}
console.log(useranme); // 

```
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable `username` is insiade an object {} with const that creates a  block scope and we can't access the variable defined inside a object from outside.

The above code will throw an error `Reference Error username is not defined`.


3. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  let username = 'Arya';
}
console.log(useranme); // output
```
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable `username` is insiade an object {} with an if statement when it is true and it is defined with
let that create block scope. so when we execute `username` that is not in global scope 

The above code will throw an error `Reference Error username is not defined`.


4. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
if (true) {
  var username = 'Arya';
}
console.log(useranme); // output

```
In above code we are looking for the variable named `username`. There is no variable named `username` in the global scope. The variable `username` is insiade an object {} with an if statement when it is true and it is defined with
var that create global scope. so when we execute `username` that is in global scope the value can be acessed outside but there is typo error `useranme` so 

The above code will throw an error `Reference Error username is not defined`.


5. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  var username = 'Arya';
}
console.log(useranme); // output
```
In above code we are looking for the variable named `username`. There is a variable named `username` in the global scope. with let that creates a block scope now there is an {} with if statement true  that has username with var variable that creates global scope and initialised its value to undefined.
now when we will call username in execution state it will look for its value as username has already been declared in global scope

The above code will throw an error `Uncaught SyntaxError: Identifier 'username' has already been declared`.

6. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
if (true) {
  let username = 'Arya';
}
console.log(useranme); // output

```
In above code we are looking for the variable named `username`. There is a variable named `username` in the global scope. with let that creates a block scope now there is an {} with if statement true  that has username with let  that creates block scope and initialised its value to empty.
now when we will call username in execution state it will look for its value as username in global scope that is empty


The above code will throw an error `Reference Error username is not defined`.


7. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
let username = 'John';
function sayHello() {
  let username = 'Arya';
}
sayHello();
console.log(useranme); // output

```
gec
In above code we are looking for the variable named `username`. There is a variable named `username` in the global scope. with let that create a block scope. then there is a fn sayHello that has fn definiation.
fec
sayHello in memory that has username "enpty" and no return statement so when we call it or execute it willnot return anything
so when we execute `username` that is in global scope the value can be acessed outside but there is typo error
 `useranme` so 

The above code will throw an error `Reference Error useranme is not defined`.

8. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (var i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // output
```
The for loop initializes the variable i with 0 using var before the loop starts. The variable i is function-scoped or global-scoped 

The loop condition is i < 10, and as long as the condition is true, the loop body will execute.

Inside the loop body, we have a console.log statement that prints the value of i along with the string 'First'.

During each iteration of the loop, the value of i will be printed along with the string 'First'.

After the loop completes, the value of i will be 10 because that is the value that caused the loop to terminate (when i < 10 becomes false).

The code proceeds to the second console.log statement outside the loop.

When the second console.log(i, 'Second') statement is executed, the code looks for the variable i in the current scope (global scope) because it is not defined within the console.log block.

Since the variable i is declared with var in the global scope, it is accessible outside the loop as well.

The above code will have following result
0 First
1 First
2 First
3 First
4 First
5 First
6 First
7 First
8 First
9 First
10 Second


9. Go through the code below and write down the process of making decision about looking for the variable. Also write the output of the code below.

```js
for (let i = 0; i < 10; i++) {
  console.log(i, 'First'); // output
}
console.log(i, 'Second'); // output
```
The for loop initializes the variable i with 0 using let before the loop starts. The variable i is block-scoped, which means it is only accessible within the for loop's block.

The loop condition is i < 10, and as long as the condition is true, the loop body will execute.

Inside the loop body, we have a console.log statement that prints the value of i along with the string 'First'.

During each iteration of the loop, the value of i will be printed along with the string 'First'.

After the loop completes, the variable i goes out of scope because it was declared with let, and the scope of i is limited to the for loop.

The code proceeds to the second console.log statement outside the loop.

When the second console.log(i, 'Second') statement is executed, the code looks for the variable i in the current scope (global scope) because it is not defined within the console.log block.

Since the variable i was declared with let and its scope is limited to the for loop, it is not accessible outside the loop, and this will result in a ReferenceError

the above code will produce 
0 First
1 First
2 First
3 First
4 First
5 First
6 First
7 First
8 First
9 First
ReferenceError: i is not defined
