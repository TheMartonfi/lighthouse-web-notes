## Types of testing

  * ### Unit testing
  `Unit testing` is the `practice` of testing small pieces of code, typically `individual functions`.

  * ### Integration Testing
  As the name suggests, in `integration testing` the idea is to test how `parts of the system work together` – the integration of the parts. `Integration tests` are `similar` to `unit tests`, but there’s `one big difference`: while `unit tests` are isolated from other components, `integration tests are not`. For example, a unit test for database access code would not talk to a real database, but an integration test would.

  * ### Functional Testing
  `Functional testing` is also sometimes called `E2E testing`, or `browser testing`. Functional testing is `defined` as the `testing of complete functionality` of some application.

## Unit testing

Create a `test` folder in your project folder. Your test `case` will go `here`.

Run this `npm command` in the `root directory` of your `project`.

```
npm install mocha chai --save-dev
```

## Using npm test

* Run `npm init` to setup a `new package.json` file.
* `Update` the `scripts` in the `package.json` to include the following test script.

```json
"scripts": {
  "test": "./node_modules/mocha/bin/mocha"
  ```
* Now we can run `npm test` every time we want to `run` all the `tests`

## Syntax to run automated testing.

```javascript
const chai = require('chai');
const assert = chai.assert;

const myFunctionToTest = require('./pathToMyFunction');

describe("myFunctionToTest()", function() {

  it("should return true for the given input compared to value expected", function() {
    const input = 'input';
    const expectedOutput = 'expected output';

    assert.isTrue(myFunctionToTest(input), output);
  });

});
```





