* [Mozilla Developer Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures)
    * An innner function has access to an outer function's variables
    * The example below will display `Mozilla` since `displayName()` has access to `init()` variables.
    ```javascript
        function init() {
        var name = 'Mozilla'; // name is a local variable created by init
        function displayName() { // displayName() is the inner function, a closure
            alert(name); // use variable declared in the parent function
        }
        displayName();
        }
        init();
    ```
    * Lexical scoping refers to when a variable or function is defined or declared - not invovoked.
    * [Code Pen example for function factory](https://codepen.io/kevinfieroshopify/pen/XWeWdvJ)
* [Lexical Scope Tutorial](https://www.freecodecamp.org/news/javascript-lexical-scope-tutorial/)
    * [Code Pen Closure Example](https://codepen.io/kevinfieroshopify/pen/Yzrzwbz)
    * Lexical scope is defined as where something is defined. The `myName` variable is considered a global lexical scope for this reason in the below example:
    ```javascript
        // Define a variable in the global scope:
        const myName = "Kevin";

        // Call myName variable from a function:
        function getName() {
        return myName;
        }
    ```
    * In the below example the lexical scope is in the local `getName()` function:
    ```javascript
        function getName() {
        const myName = "Oluwatobi";
        return myName;
        }
    ```
    * Scopes that do not have access to a variable in a different scope will throw an `Uncaught Reference Error` error when trying to access them since the scope does not think the variable is defined. 
    * Children have access to parent's scope but not vice-versa. Sibling spaces do not have access to each other's scope.
    * [Code Pen example](https://codepen.io/kevinfieroshopify/pen/XWeWdRQ)
    * [Closure Video Example](https://www.youtube.com/watch?v=71AtaJpJHw0&ab_channel=techsith)