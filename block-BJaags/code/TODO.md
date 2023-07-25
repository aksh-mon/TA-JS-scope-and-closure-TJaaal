To create the execution context diagram consider the following:

- Global and Function Execution Context
- Different Phases Of Execution Context
- Var let and const

Create the execution context diagram of the following code line by line.

```js
let num = 21;
function square(num) {
  return num * num;
}
let hundred = square(10);
console.log(hundred);

![Image 1](img/image-01.jpg)

```

Create the execution context diagram of the following code line by line.

```js
var num = 21;
function addFive(n) {
  return n + 5;
}
var five = addFive(0);
var ten = addFive(5);
console.log(five, ten);

![Image 2](img/image-02.jpg)

```

Create the execution context diagram of the following code line by line.

```js
let marks = [34, 45, 56, 76];
function multiplyArrayByN(arr, n) {
  let finalArr = [];
  for (let elm of arr) {
    finalArr.push(elm * 2);
  }
  return finalArr;
}

let numbers = multiplyArrayByN(marks);
console.log(numbers);

![Image 3](img/image-03.jpg)

```

Create the execution context diagram of the following code line by line.

```js
counter();
function counter(){
  let count = 0;
  function increment(){
    return count++;
  }
  return increment()
}

![Image 4](img/image-04.jpg)

```

Create the execution context diagram of the following code line by line.

```js
counter();
let counter = function () {
  let count = 0;
  function increment() {
    return count++;
  }
  return increment();
};

![Image 5](img/image-05.jpg)

```
