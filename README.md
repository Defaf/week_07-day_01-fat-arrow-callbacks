# Week 07 Day 01 - Fat Arrow Callbacks

## Arrow Functions

We frequently use `arrow` (sometimes referred to as `fat arrow`) functions as
callbacks (which we will define next).  This is convenient when the callback is
simple and anonymous.

### How to Convert to Arrow Syntax

We can convert an existing JavaScript function to use the arrow syntax with the following steps.

1. Remove the `function` keyword
2. Add a fat arrow (`=>`) between the function parameters  `()` and the opening brace `{`

```js
// Without arrow syntax

const helloWorld = function () {
  console.log('Hello World!')
}

const add = function (num1, num2) {
  return num1 + num2
}

// Using arrow syntax

const helloWorld = () => {
  console.log('Hello World!')
}

const add = (num1, num2) => {
  return num1 + num2
}
```

### Single Expression Implicit Return

Arrow functions bodies that are a single expression have an added benefit, an
implicit return.  This means that arrow function bodies without `{}` return the
value of the expression without needing to use `return`.

```js
// Without arrow syntax
const add = function (x, y) {
  return x + y
}

// Using arrow syntax with an explicit return
const add = (x, y) => {
  return x + y
}

// Using arrow syntax with an implicit return
const add = (x, y) => x + y
```

### Single Parameter

When using the arrow function syntax with a single parameter, then parenthesis are not required.

```js
// Without arrow syntax
const isPositive = function (num) {
  return num > 0
}

// Using arrow syntax with an implicit return value
const isPositive = (num) => num > 0

// Parenthesis aren't required for a single parameter
const isPositive = num => num > 0
```
