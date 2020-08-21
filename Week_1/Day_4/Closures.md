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

## Using Closures II

```javascript
// Create a function called wrapLog() that takes in a function (callback) and a string (name)
// and returns a function that internally invokes (calls) callback during its execution 
// and also logs the name, input parameters, and return value of the callback function.

const wrapLog = (callback, name) => {

  return function()  {

    callback();
    let paramaters = [];

    //You cannot use arguments with arrow declaration function
    for (const paramater of arguments) {
      paramaters.push(paramater);
    }

    console.log(`${name}(${paramaters.join(', ')}) => ${callback.apply(null, paramaters)}`);
    
  };

};

const area = function (x, y) {
  return x * y;
};

const logArea = wrapLog(area, "area");

logArea(5, 3); // area(5, 3) => 15
logArea(3, 2); // area(3, 2) => 6

const volume = function (x, y, z) {
  return x * y * z;
};
const logVolume = wrapLog(volume, "volume");

logVolume(5, 3, 2); // volume(5, 3, 2) => 30
logVolume(3, 2, 4); // volume(3, 2, 4) => 24
```