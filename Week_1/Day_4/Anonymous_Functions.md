## Anonymous Functions

Anonymous functions are often `declared` while being passed in as `callbacks` to other functions. Why? Because the receiving function that takes in the anonymous function will give that parameter a name anyway.

```javascript
["Alice", "Bob", "Waldo", "Winston"].forEach((elem, index) => {
  if (elem === 'Waldo') {
    console.log("Found him! At index: ", index);
  }
});
```