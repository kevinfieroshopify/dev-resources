* [Prototypes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
    * Example:

        ```
        // Let's create an object o from function F with its own properties a and b:
        const F = function () {
        this.a = 1;
        this.b = 2;
        };
        const o = new F(); // { a: 1, b: 2 }

        // add properties in F function's prototype
        F.prototype.b = 3;
        F.prototype.c = 4;

        ```
        * console.log(o.a); // 1
        * console.log(o.b); // 2
            * Illustrates [Property Shadowing](https://medium.com/piecesofcode/javascript-objects-property-shadowing-66159b143b2)
        * console.log(o.c); // 4
        * console.log(o.d); // undefined
            * Does not exist on either.
    * This can apply to methods as well.


