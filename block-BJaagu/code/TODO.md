Find the output of the code snippets below:

```js
console.log(numA + numB); //NaN
var numA = 21,
  numB = 30;
```
![image-01](img/image-01.png)

Find the output of the code snippets below:

```js
console.log(numA + numB); // Uncaught ReferenceError: numA is not defined
let numA = 21,
  numB = 30;

```
![image-02](img/image-02.png)

Find the output of the code snippets below:

```js
let numA = 21,
  numB = 30;
console.log(numA + numB); // 51

```
![image-03](img/image-03.png)

Find the output of the code snippets below:

```js
console.log(sayHello()); // Hello

function sayHello() {
  console.log("Hey");
}

function sayHello() {
  console.log("Hello");
}

```

![image-04](img/image-04.png)

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // Tyrion
function sayHello() {
  console.log(username);
}

```
![image-05](img/image-05.png)

Find the output of the code snippets below:

```js
sayHello(); //  ReferenceError: username is not defined at sayHello 
let username = "Tyrion";
function sayHello() {
  console.log(username);
}
```

![image-06](img/image-06png)

Find the output of the code snippets below:

```js
let username = "Tyrion";
sayHello(); // sayHello is not defined
let sayHello = () => {
  console.log(username);
};
```
![image-07](img/image-07.png)

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
let username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```

![image-08](img/image-08.png)

Find the output of the code snippets below:

```js
sayHello(); // sayHello is not defined
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
};
```

![image-09](img/image-09.png)

Find the output of the code snippets below:

```js
var username = "Tyrion";
sayHello(); //  sayHello is not defined
let sayHello = () => {
  console.log(username);
};
```

![image-10](img/image-10.png)

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  var username = "John";
};
sayHello(); // undefined

```

![image-11](img/image-11.png)

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  var username = "John";
  console.log(username);
};
sayHello(); // john


```
![image-12](img/image-12.png)

Find the output of the code snippets below:

```js
var username = "Tyrion";
let sayHello = () => {
  console.log(username);
  let username = "John";
};
sayHello(); // ReferenceError: Cannot access 'username' before initialization

```