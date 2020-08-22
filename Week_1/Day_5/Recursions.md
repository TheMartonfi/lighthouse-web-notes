## Recursions

`Recursion` is an `alternative` to `traditional looping` that allows you to do the same thing, just in a slightly different way. Recursion isn't necessarily a better way of doing this, it's just a different way of doing this.

Any problem that you can `solve` with a for `loop`, you can `solve` with `recursion`, and vice versa.

```javascript
function countEvenToTwelve(number) {
  if (number <= 12) { // Recursive Case
    console.log(number);
    // The function will call itself again and get closer to the base case
    countEvenToTwelve(number+2);
  }
  // Base case, do nothing when number > 12
}
countEvenToTwelve(0);
```

The `recursive case` is when the `function will continue to call itself`. Every time the function calls itself, the `input` gets `closer` and closer to the `base case`. The `base case` is when the `function no longer calls itself`. In a properly designed `recursive function`, with each recursive call, the `input must gradually resolve toward the base case`.

