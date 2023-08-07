1. What does thread of execution means in JavaScript?
In JavaScript, a thread of execution refers to the sequential execution of code within a JavaScript program. It represents the path of execution as the program runs, step by step, through the instructions in the code.

JavaScript is single-threaded, meaning it can only execute one set of instructions at a time. This differs from multi-threaded programming languages, where multiple threads can run simultaneously, executing different parts of the code concurrently.

In JavaScript, the thread of execution starts at the beginning of the program and follows the execution flow line by line, statement by statement. It performs tasks such as variable assignments, function calls, and calculations in the order they appear in the code. As each task is completed, the thread moves on to the next one.


2. Where the JavaScript code gets executed?

JavaScript code gets executed within the context of an execution environment, and one of the fundamental execution contexts is the global execution context.

The global execution context represents the top-level scope in which JavaScript code is executed. It is created when the JavaScript engine starts running the code and remains active throughout the entire runtime. The global execution context has a global object associated with it, which serves as the container for global variables, functions, and other constructs defined in the code.

3. What does context means in Global Execution Context?

In the context of global execution context, the term "context" refers to the environment or scope in which JavaScript code is executed at the global level. It represents the global scope, where variables, functions, and objects are defined and accessible throughout the entire program.

The global execution context is created when a JavaScript program starts running and remains active until the program terminates. It consists of two main components:

Global Object: In a browser environment, the global object is typically the window object, whereas in Node.js, it is the global object. The global object provides a set of built-in properties and methods that can be accessed from anywhere in the code.

Global Scope: The global scope refers to the outermost scope of a JavaScript program. Variables and functions declared outside of any function or block are considered part of the global scope and can be accessed from anywhere within the program.

4. When do you create a global execution context.

The global execution context is automatically created when a JavaScript program starts running. It is the first execution context to be created and serves as the foundation for executing the code.

5. Execution context consists of what all things?

An execution context in JavaScript consists of several components that define the environment in which code is executed. These components include:

Variable Environment: It contains all the variables and function declarations defined within the current scope. This includes function arguments, local variables, and function declarations (hoisted functions). The variable environment also holds references to outer environments, allowing access to variables in higher-level scopes.

Lexical Environment: It is similar to the variable environment and holds the same information. However, the lexical environment is used for static scoping and is immutable, while the variable environment can be modified during execution.

This Value: The this value refers to the object to which a function or method belongs. It provides a way to access and manipulate properties and methods within the current context.

Outer Environment: This component references the surrounding or parent scope of the current execution context. It allows access to variables and functions in higher-level scopes. In the case of a global execution context, the outer environment is usually null.

6. What are the different types of execution context?

In JavaScript, there are two main types of execution contexts:

Global Execution Context: The global execution context is created when a JavaScript program starts running. It represents the global scope and is associated with the entire script or module. The global execution context includes the global object (window object in browsers, global object in Node.js), the global scope, and all the variables and functions declared in the global scope.

Function Execution Context: A function execution context is created each time a function is called or invoked. It represents the local scope of the function and includes the function's arguments, local variables, and inner function declarations. Each function invocation creates a new function execution context, forming a stack of contexts known as the "call stack."

7. When global and function execution context gets created?

 The global execution context is created when the JavaScript program starts running, while function execution contexts are created dynamically each time a function is called or invoked. The global execution context represents the global scope, whereas function execution contexts represent the local scope of individual functions.

8. Function execution gets created during function execution or while declaring a function.

Function execution contexts are created dynamically when a function is called or invoked, not during the declaration of the function itself.

When a function is declared in JavaScript, it defines the function's behavior and establishes its presence in the global or local scope. However, the function execution context is not created at this point. It is only created when the function is actually called or invoked in the code.

9. Create a execution context diagram of the following code on your notebook. Take a screenshot/photo and store it in the folder named `img`. Use `![](./img/image-name.png)` to display it here.


``
```js
var user = "Arya";

function sayHello(){
  return `Hello ${user}`;
}

var userMsg = sayHello(user);

```

<!-- Put your image here -->

![](./img/img-01.jpg)



```js
var marks = 400;
var total = 500;

function getPercentage(amount, totalAmount){
 return (amount * 100) / totalAmount;
}

var percentageMarks = getPercentage(marks, total);
var percentageProfit = getPercentage(400, 200);


```

<!-- Put your image here -->

![](./img/img-02.jpg)



```js
var age = 21;

function customeMessage(userAge){
  if(userAge > 18){
    return `You are an adult`;
  }else {
    return `You are a kid`;
  }
}

var whoAmI = customeMessage(age);
var whoAmIAgain = customeMessage(12);
```

<!-- Put your image here -->

![](./img/img-03.jpg)