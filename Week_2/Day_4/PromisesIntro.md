## Promises Intro

### Summary

Promises are not an overly complicated subject, but can take a long time to fully understand. 

A promise represents the eventual result of an asyncronous operation. The primary way or interaction with a promise is through its "then" method, which registers callbacks to reiver either a promise's eventual value or the reason why the promise cannot be fulfilled.

We don't avoid callbacks with promises, instead we wrap them into a promise.
 
* A promise is an object
* Promises do not rely on anything other than basic JavaScript
* As of ES6, JavaScript has promises supported natively in its code (Promises are built into the language).