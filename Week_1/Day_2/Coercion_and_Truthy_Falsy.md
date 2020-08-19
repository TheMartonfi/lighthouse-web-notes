## Double Equals, Triple Equals, and Type Coercion

We can use either the `===` operator, or the `==` operator. Up to this point, we've been exclusively using the `===` to compare two values, and with good reason. The `===` does not only compare two values, but also the type of those values.

## Falsey Values

```javascript
// All of the following are inherently falsey:

False
// False is False. Makes sense, right?

0
// 0 is the only falsey Number

""
// an empty string is falsey

null
// a null, or empty value, is falsey.

undefined
// an object that has not been defined is considered falsey.

NaN
// Not a Number. You'll learn more about NaN as we go on.
```

[Reading](https://stackoverflow.com/questions/359494/which-equals-operator-vs-should-be-used-in-javascript-comparisons/359509#359509) on comparison operators.