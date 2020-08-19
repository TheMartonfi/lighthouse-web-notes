## Syntax Errors

```javascript
var rank = "Imperator";
var name = "Furiosa";

console.log(rank name);
```

If we execute the above code, then our `output` would resemble the following.


node syntax-error.js
/vagrant/w1d2/syntax-error.`js:4`
`console.log(rank name);`
                 ^^^^
`SyntaxError: Unexpected identifier`
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3


This bit is called a `stack trace`, which shows the state of our program `when the error occurred`.






