* [Hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting)
    * Hoisting allows you to call a function or variable before it is declared.
    * Without this it would be required that declarations occur in the file before the function or variable is called.
    * `var` **declarations** can be hoisted but not **initializations**. This means the variable will always have an `undefined` value until the line of code is executed in the file.
    * `let` and `const` will not be given a value of `undefined` but rather `Throws ReferenceError exception as the variable value is uninitialized` error will occur. So it is technically hoisted but it is not initialized so can not be accessed.

* [CodePen Example](https://codepen.io/kevinfieroshopify/pen/PoJJXRE)

```javascript
example(); // function is called because it is hoisted

function example() {
  console.log("example function");
}

console.log(variable); // var variable is logged as undefined until intialized
var variable = 10;
console.log(variable); // var variable is logged as 10 after initialized

console.log(letVariable); // let variable throw an Uncaught ReferenceError if not defined beforehand. Stops code execution
let letVariable = 5;
console.log(letVariable);
```

Interesting Articles:
* [StackOverflow: Are Variables Declared With Let Or Const Hoisted?](https://stackoverflow.com/questions/31219420/are-variables-declared-with-let-or-const-hoisted)
* [Hoisting in Modern JavaScript — let, const, and var](https://blog.bitsrc.io/hoisting-in-modern-javascript-let-const-and-var-b290405adfda)