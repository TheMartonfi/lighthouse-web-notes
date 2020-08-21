## Higher Order Functions

`Functions` that take in `callbacks` are referred to as `Higher Order Functions`.

Functions such as `forEach`, `filter`, `map` and others can be called "`Higher-Order Functions`".

```javascript
const grades = [73, 69, 3, 100, 50, 70, 69, 88, 95, 77, 35];

const passingGrades = grades.filter(grade => {
  return grade >= 70;
});
```