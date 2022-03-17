* [Optional Chaining](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
    * Using to check a nested property without worrying about whether some properties are null or undefined along the way.
    * By using `?.` we can look at `animal?.dog?.name` without worrying if `dog` exists. An undefined will be returned rather than throwing an error. 
    * Alternative syntax for the above example without using optional chaining would be `let example = obj.first && obj.first.second`.
    * This can be used with function calls as well for possibly undeclared functions.
    * Can return a different value other than undefined by using the nullish coalescing operator `const customerCity = customer?.city ?? "Unknown city"`