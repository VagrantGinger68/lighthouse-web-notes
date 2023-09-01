## setTimeout intro

### Summary
setTimeout is an example of asynchronous programming in JavaScript. It is used to delay the execution of code to later. We tell it what to delay with a callback function and a delay in ms.

</br>

An example of setTimeout looks like:
```js
console.log('first line');
setTimeout(() => {
  console.log('timeout line');
}, 1000);
console.log('last line');
```
It will output 'first line', then 'last line', then 'timeout line' because it runs the entire function, then goes back to the delayed section.

</br>

Some examples of setTimeout are: 
1. A website showing a chat box shortly after opening the page.
2. A site that pops up a notice then hides it after a few seconds.
3. An adblocker popup that asks you to disable it on certain sites.
