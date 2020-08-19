## Global vs Local Scopes

A globally-scoped variable is available everywhere in the code, whereas a locally-scoped variable would only be available within the function in which it's defined.

```javascript
let myVar = "global";

const myFunction = function() {
  let myVar = "local";

  console.log("inside myFunction, myVar is:", myVar); 
}

myFunction();

console.log("outside myFunction, myVar is:", myVar);  
```

The first console.log will set myVar to local and the second will set myVar to global.

## Pass In the Data Needed

It is ideal if functions try to `avoid reading outer scope variables`. If a function needs some information / data, then that `data should instead be passed in as a parameter`, making it available within the function's inner scope.

```javascript
const person = "Martha";

// BAD
const sayHelloBadly = function() {
  console.log(`Howdy, ${person}`);
}
sayHelloBadly(); // Works, but not ideal!

// GOOD
const sayHelloGoodly = function(name) {
  console.log(`Howdy, ${name}`);
}
sayHelloGoodly(person);
```