## Promises Intro

### Summary

Promises are not an overly complicated subject, but can take a long time to fully understand. 

A promise represents the eventual result of an asyncronous operation. The primary way or interaction with a promise is through its "then" method, which registers callbacks to reiver either a promise's eventual value or the reason why the promise cannot be fulfilled.

We don't avoid callbacks with promises, instead we wrap them into a promise.
 
* A promise is an object
* Promises do not rely on anything other than basic JavaScript
* As of ES6, JavaScript has promises supported natively in its code (Promises are built into the language).

</br>

A promise is an object which represents a task that will execute and the result of the task. We can add callbacks to the promise to handle the results.

</br>

Examples:
```js
gotoTheirHouse(billy, () => {
  pretendToBeFriends(billy, () => {
    stealWhenNotLooking(billy.mixtapes, (items) => {
      hideInBackpack(items, () => {
        console.log("I don't feel well. I gotta go home now Billy!");
      });
    });
  });
});
```

with promises, the same code would look like this:
```js
gotoTheirHouse(billy)
  .then(pretendToBeFriends)
  .then(stealWhenNotLooking)
  .then(hideInBackpack)
  .then(() => {
    console.log("I don't feel well. I gotta go home now Billy!");
  });
```

</br>

Other benefits of promises are that error handling becomes much simpler, they make asynchronous code easier to unit test, and Promise.all can be used to run miltiple async operations in parallel and have a single callback to see all the results.