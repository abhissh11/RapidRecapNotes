# JavaScript

JavaScript is synchronous single threaded language.
Absolutely! JavaScript operates on a single thread, using an event-driven, nonblocking model. This means it can handle asynchronous operations efficiently,
making it great for tasks like handling user input, making API calls, and
managing events.

- So, JavaScript being single-threaded means it has only one execution thread in
  which it processes code. This might sound limiting, but it actually helps keep
  things simple and avoids certain types of bugs.

- Now, when it comes to asynchronous behavior, JavaScript uses something
  called the event loop. The event loop continuously checks the message queue
  for any pending messages or events. When an asynchronous operation, like
  fetching data or handling a user click, is completed, a message is pushed to the
  queue.

- Here's the cool part: JavaScript doesn't wait for these asynchronous tasks to
  finish. It just moves on with its single thread, and when the asynchronous
  operation is done, it's added to the message queue. The event loop then picks
  it up and processes it.
- This non-blocking nature allows for smooth user interactions and efficient
  handling of tasks without freezing up the entire program. Pretty neat, huh?

# Execution Context in JavaScript

Everything in JavaScript happens in Execution Context.

Execution context in JavaScript is the environment in which JavaScript code is executed. It contains information about the current scope, variables, and functions.

**_ How code is excuted in JS _**

- In the first phase of execution JS scans whole code and allocates memory to every JS components(variables, functions, etc.). During this phase the memory is allocated and asigned a special keyword _undefined_ to each variable present to be executed in **_global Execution Context_**. And to each of the functions the function, whole content of each functions are set as it is in global Execution context.

- In the second phase, running from top to end each variables are assigned their actual value replacing from undefined keyword. And for each functions:
- - Each time a function is called, a new execution context is created.

## The execution context for function contains the following info:

- The Current Scope : This is the scope in which the function is called.

- The Variables : This is the list of all the variables that are accessible to the function in it's scope.

- The Functions : This is a list of all the functions that are accessible to the function.

The execution context for a function is destroyed when the function returns.

## There are two types of Execution Context in JS:

- Global Execution Context : This is the execution context for the global scope. It is created when the JS engine starts up.

- Function Execution Context : This is the execution context for a function. It is created whenn the function is called. This is pushed to the **_ Call Stack_** where Global Execution Context is already present.

## How Execution Context works :

- When a function is called, a new execution context is created. The new EC is pushed onto the stack.
  when the function returns, its execution context is popped off the stack.

- The Stack of EC is used to keep track of the current scope and the variables and function that are accessible to the current code.

Example :

```bash
function greet(name) {
 console.log("Hello, ${name}!");
}

greet("Abhishek");


```

When the greet() function is called, a new EC is created. The new EC contains following info :

- The Current Scope : this is the global scope.

- The Variables : This is the list of vars that are accessible to the greet() function, including the _name_ parameter.

- The Functions : This is a list of all the functions that are accessible to the _greet()_ function, including the _console.log()_ function.

The greet() function thenn prints a greeting to the console. When the greet() function returns, it's EC is popped off the Stack.

**_ After the whole program is executed/finished, the global EC will also be popped off. _**

**_ Call Stack(also known as Program Stack, Control Stack, Runtime Stack, Machine Stack) maintains the order of execution of EC. _**
