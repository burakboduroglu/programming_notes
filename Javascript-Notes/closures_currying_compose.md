### Javascript Closure, Currying and Compose

## `Closure:`
- A closure is a function having access to the parent scope, even after the parent function has closed.
- Example:
```javascript
function outer() {
  let a = 10;
  function inner() {
    console.log(a);
  }
  return inner;
}
const innerFn = outer();
innerFn(); // 10
```
- In the above example, the inner function has access to the variable a, even after the outer function has returned. This is because of closure.

## `Currying:`
- Currying is a technique of evaluating function with multiple arguments, into sequence of functions with single argument.
- Example:
```javascript
function curriedAdd(a) {
  return function(b) {
    return a + b;
  }
}
const add5 = curriedAdd(5);
add5(10); // 15
```
- In the above example, the curriedAdd function returns a function which takes a single argument and returns the sum of the argument passed to the curriedAdd function and the argument passed to the returned function.
- Example with 'Arrow Function':
```javascript
const curriedAdd = a => b => a + b;
const add5 = curriedAdd(5);
add5(10); // 15
```

## `Compose:`
- Compose is a technique of combining two or more functions to produce a new function.
- Example:
```javascript
function compose(f, g) {
  return function(a) {
    return f(g(a));
  }
}
const sum = num => num + 1;
const multiply = num => num * 2;
const multiplyAndSum = compose(sum, multiply);
multiplyAndSum(5); // 11
```
- In the above example, the compose function takes two functions as arguments and returns a new function which takes a single argument and returns the result of the first function applied to the result of the second function applied to the argument.
- Example with 'Arrow Function':
```javascript
const compose = (f, g) => a => f(g(a));
const sum = num => num + 1;
const multiply = num => num * 2;
const multiplyAndSum = compose(sum, multiply);
multiplyAndSum(5); // 11
```
✅ If you like this article, you can give me a star on. 😎
Thanks for reading. 🙏