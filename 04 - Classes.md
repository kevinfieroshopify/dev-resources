* [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
    * Class Declaration
    ```javascript
    class Rectangle {
        constructor(height, width) {
        this.height = height;
        this.width = width;
        }
    }
    ```
    * Classes must be defined before they are constructed. The values are hoisted but needs to be initialized before it is used. For example the below code will work. However, reversing the order would throw a `ReferenceError: Cannot access 'Rectangle' before initialization`
    ```javascript

    class Rectangle {
        constructor(height, width) {
            this.height = height;
            this.width = width;
        }
    }

    const p = new Rectangle(5, 5);
    ```
    * Prototype methods such as getters and setters are used to retrieve and set class property values.
    * Static methods can not be used on an instance of a class but rather the class itself.
    * Can declare a default value:
    ```javascript
        class Rectangle {
            height = 0;
            width;
            constructor(height, width) {
                this.height = height;
                this.width = width;
            }
        }
    ```
    * Private variables are used by using `#` in front of the variable name. These can only be accessed internally within the class.
    * Extends allows classes to inherit properties from another class.
        * Another resource on class inheritance: [LINK](https://javascript.info/class-inheritance)