## Automated Testing

### Summary
We learned about how to write automated tests for our code so that we can save time compared to testing after each code change. We used Mocha and Chai to build the tests.

</br>

### Benefits of automated testing
1. It saves time because we dont have to manually run tests multiple times.
2. It makes it easier to see how a new piece of code works because we can analyze the expected results of the test.
3. It allows us to not keep everthing in our heads at once. We can focus on the current function implementation and the tests can tell us if something breaks in the process.

</br>

### JS examples
Here is how you would start a test document with Chai:
```js
const chai = require('chai');  // import the chai library
const assert = chai.expect;  // establish a variable to be used in our tests
```

The function we are testing needs to be imported into the test file:
```js
const validator = require('../javascript/groupValidator.js'); // import the file where our function lives
```

Then we have to describe what the function should do:
```js
describe("The function groupValidator()", () => {
    // this is where we put our tests.
});
```

Inside the describe block, we write "it" statements that describe the expected result, and write a function that will test the function against the expected result:
```js
 it("should return true if there are between 2 and 5 group members", () => {
    assert(validator.isGroupValid(["a", "b", "c"])).to.be.true
  });
```
