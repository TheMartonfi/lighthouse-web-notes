## Functions As Object Properties aka Methods

Instead of assigning just data values, object `properties` can be `assigned function values`.

```javascript
const person = {
  firstName: 'Bob',
  lastName:  'Smith',
  fullName: function() {
    return this.firstName + ' ' + this.lastName;
  }
}

// Nice, now I can just say:
console.log('Hello, ' + person.fullName());
// And it's much "cleaner" every time I need their full name!
```

For now you can think of `this` only needing to be used inside `methods` like fullName of person. In that situation, when used `within an object's method`, this `points` to the `object` where its `function resides`.
How this is defined on [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)

## Arrow functions and this

```javascript
const arrowFunction = (paramter) => {
  //function code
};
```

* Arrow Function syntax can vary based on how simple the function is
* `Arrow functions` don't get assigned a value for `this` (in the way that traditional function expressions do).
* This"`limitation`" is in fact `intentional`, and can be used as an `advantage` in certain situations - situations where it is beneficial to `inherit` the `value` of this from its `lexical scope`. Such as the this.firstName being read in the sayHello method.


