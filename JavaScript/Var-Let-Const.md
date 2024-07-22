# Var Let and Const in JS

Var, let, and const are the three main ways to declare variables in JavaScript. To produce clear and manageable code, it’s crucial to be aware of how these keywords differ from one another. Each of these keywords has a certain purpose and has a distinct scope. We shall examine the differences between var, let, and const in JavaScript

## Var

Since the birth of JavaScript, var has been the most traditional method of declearing variables. Var-declared variables are function-scoped, which means their scope is constrained to the function in which they are specified.
It will still be possible to acess a variable that is declared using var keyword inside a block, such as loop or conditional expression.

Example:

```bash
function exampleVar() {
  if (true) {
    var x = 10;
  }
  console.log(x); // Outputs 10
}

exampleVar();

```

In the above example, X is declareed using var inside the if block, but it is still accessible outside when we log it to the console.

## Let

let was added in ECMAScript 6 (ES6), offers a more consistent and block-scoped method of declaring variables.
let declaration limit variables to the block where they are specified. Because of this, let is especially helpful for preventing unintentional variable hoisting and lowering the possibilities of scope-related errors.

Example:

```bash
function exampleLet(){
    if(true){
        let y = 20;
    }
    console.log(y);     // Throws a ReferenceError : y is not defined.
}

exampleleLet();
```

In the above example, y is declared using let inside the if block, and is not accessible outside the block. Attempting to log y outside the block results in a ReferenceError.

## const

const are variables that cannot have their initial value changed.
Constarainted to the block in which it is defined, const is a block-scoped, like let.
const is thus a good choice for declaring variables that should not change while a block of code is being executed.

Example:

```bash
function exampleConst(){
    const z = 20;
    z = 40;         // Throws a TypeError: Assignment to constant variable
}

exampleConst()
```

In the above example, z is declared using const and is immediately assigned the value 20. When we try to reassign it to z = 40, a TypeError is thrown, bcz const variable can not be reassigned.

# Summary:

var, let and const are three different ways of declaring variables in JS, each with its own scope and useCases:

- var is function-scoped and has been around since the early days of JS.
- let is block-soped and was introduced in ES6, offering a more predicatble scoping mechanism.
- const is also block-scoped and is used to declared constants that cannot be reassigned after intialization.

## Important Note about let & const

- let and const are hoisted but its memory is allocated at other place than window which cannot be accessed before initialization.

- Temporal Dead Zone (TDZ) exists until variable is declared and assigned a value.

- Widow.variable OR this.variable will not give value of variable defined using let or const.

- We cannot redeclare the same variable with let/const (even with using var the seond time declaration is forbade).

- const variable declaration and initializaion must be done on the same line.

## Three Types of Errors

1. ReferenceError : given where variable does not have memory allocation.
2. TypeError : given when we change type that is not supposed to be changed. (while trying to re-initialize const variable).
3. SyntaxError : given when proper syntax is not used.

- Use const whenever possible followed by let, use var a little as possible (only if you have to) -> It helps avoiding error.
- Initialzing variables at the top is good practice helps shrinking TDZ to zero.
