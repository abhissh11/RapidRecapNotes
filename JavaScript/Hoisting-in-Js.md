# Hoisting in JavaScript

Hoisting mechanism in JavaScript where the variable declarations are moved to the top of the scope before execution. Therefore, it is possible to call a function before initalizing it.

- Whenever a JS program is run, a **_global execution context block_** is created, which comprises of _Memory Creation_ and _Code Execution_ phases.

Hoisting in JavaScript, where a variable and function declartation are moved to top of their containing scope during the compilation phase, before code is executed.
This means that you can use variables and functions before they are declared in your code. However, it’s important to note that only the declarations are hoisted, not the initializations or assignments.

## Variable Hoisting:

```bash
console.log(x);         //outputs undefined
var x = 5;
console.log(x)      //outputs 5
```

In the example above, even though console.log(x) in first line appears before the var declaration var x = 5; there is no error.
This is because var x is hoisted to the top of the scope, but the initialization (=5) is not hoisted. Thereefore, the first console.log(x) outputs undefined because the variable has been hoisted but not yet assigned a value.

- Variable declaration are scanned and are made undefined before declaration.

## Function Hoisting

```bash
sayHello();      // "Hello!"
function sayHello() {
  console.log("Hello!");
}
```

In this example, the function sayHello is called before its declaration, and it works. This is because the function declaration is hoisted to the top of its containing scope, allowing you to call the function before its actual placement in the code.

- It’s important to note that hoisting behavior differs between function declarations (as shown in the example above) and function expressions. Function expressions are not hoisted in the same way, and attempting to call them before their declaration will result in an error.

```bash
// Function expression
sayHi(); //         TypeError: sayHi is not a function
var sayHi = function() {
  console.log("Hi!");
};

```

In this case, the variable declaration var sayHi; is hoisted, but the function expression sayHi = function() { ... } is not, resulting in a TypeError when trying to call sayHi before its assignment.

- Functions declarations are scanned and are made available.
- Function Expression acts as Variable
- Arrow function enact as variables and get undefined during the memory allocation ( creation ) phase while functions actually get hoisted as it is.
