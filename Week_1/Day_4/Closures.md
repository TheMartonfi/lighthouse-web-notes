## Closures

When a `function` retains the `context` of a `parent function`, we call that a "`closure`".

```javascript
const outer = function() {
  const x = 10;

  const inner = function() {
    console.log("The value of x is: " + x);
  }
  return inner;
};

const foo = outer();
foo();
```
## Practical Closures

In other words, a `closure` gives you `access` to an `outer function’s scope` from an `inner function`. In JavaScript, `closures` are `created` every time a `function is created`, at function creation time.

Closures are `useful` because they let you `associate data` (the lexical environment) with a `function that operates on that data`. This has obvious parallels to object-oriented programming, where objects `allow` you to `associate data` (the object's properties) with `one or more methods`.

## Immediately-invoked function expression

You can alternatively use an `immediately-invoked function expression (IIFE)` to achieve a similar result.

```javascript
const foo = (function() {
  const x = 10;

  const inner = function() {
    console.log("Value of x is: " + x);
  }
  return inner;
})(); // Notice the () at the end,
      // which will immediately invoke the function,
      // assigning the returned value (inner) to foo

foo();
```