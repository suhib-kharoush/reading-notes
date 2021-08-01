# JavaScript

#### Syntax and Feature Overview

- ECMAScript 2015, also known as ES6, introduced many changes to JavaScript. Here is an overview of some of the most common features and syntactical differences, with comparisons to ES5 where applicable.

##### Legend:
-- Variable: `x`
- - Object: `obj`
- - Array: `arr`
- - Function: `func`
- - Parameter, method: `a, b, c`
- - String: `str`


##### Variable declaration

- ES6 introduced the `let` keyword, which allows for block-scoped variables which cannot be hoisted or redeclared.

```

var x = 0
```

```
let x = 0
```

##### Constant declaration

- ES6 introduced the `const` keyword, which cannot be redeclared or reassigned, but is not immutable.

```
const CONST_IDENTIFIER = 0 // constants are uppercase by convention
```

##### Arrow functions

- The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own `this`, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

```
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
```

```
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
```

##### Template literals

- Concatenation or string interpolation:
- - Expressions can be embedded in template literal strings.

```
var str = 'Release date: ' + date
```
```
let str = `Release Date: ${date}`
```

##### Multi-line strings

- Using template literal syntax, a JavaScript string can span multiple lines without the need for concatenation.

```
var str = 'This text ' + 'is on ' + 'multiple lines'
```

```
let str = `This text
            is on
            multiple lines`
```

##### Implicit returns
- The `return` keyword is implied and can be omitted if using arrow functions without a block body.

```
function func(a, b, c) {
  return a + b + c
}
```

```
let func = (a, b, c) => a + b + c // curly brackets must be omitted
```

##### Key or property shorthand

- ES6 introduces a shorter notation for assigning properties to variables of the same name.

```
var obj = {
  a: a,
  b: b,
}
```

```
let obj = {
  a,
  b,
}
```

##### Method definition shorthand

- The `function` keyword can be omitted when assigning methods on an object.

```
var obj = {
  a: function (c, d) {},
  b: function (e, f) {},
}
```
```
let obj = {
  a(c, d) {},
  b(e, f) {},
}
```

```
obj.a() // call method a
```

##### Destructuring

- Use curly brackets to assign properties of an object to their own variable.

```
var obj = {a: 1, b: 2, c: 3}
```

```
var a = obj.a
var b = obj.b
var c = obj.c
```

```
let {a, b, c} = obj
```

##### Array iteration

- A more concise syntax has been introduced for iteration through arrays and other iterable objects.

```
var arr = ['a', 'b', 'c']
```

```
for (var i = 0; i < arr.length; i++) {
  console.log(arr[i])
}
```

```
for (let i of arr) {
  console.log(i)
}
```

##### Default parameters

- Functions can be initialized with default parameters, which will be used only if an argument is not invoked through the function.

```
var func = function (a, b) {
  b = b === undefined ? 2 : b
  return a + b
}
```

```
let func = (a, b = 2) => {
  return a + b
}
```

```
func(10) // returns 12
func(10, 5) // returns 15
```
