## Promises Review

Promises allow us to handle asynchronous code in JavaScript. 

Synchronous code runs top to bottom, so we always know the order it will execute.

With asynchronous code, we don't know when it will finish. This could be due to slow network during a network request, or reading files from a hard drive, among many other possibilities.

JavaScript uses callbacks as default for handling asynchronous functions. A callback is when you put a function into another function as an argument. Callbacks make it more difficult to handle errors and follow the sequence of events.

With Callbacks:
```js
function loadImage (src, parent, callback){
   let img = document.createElement('img')
   img.src = src
   img.onload = callback
   parent.appendChild(img)
}

// Pyramid Of Doom with callbacks

loadImage('above-the-fold.jpg', imgContainer, function(){
   loadImage('just-below-the-fold.jpg', imgContainer2, function(){
       loadImage('farther-down-the-fold.jpg', imgContainer3, function(){
           loadImage('abstract-art.jpg', imgContainer4, function(){
               loadImage('last-one.jpg', imgContainer5)
           })
       })
   })
})

```
</br>

With Promises:
```js
const sequence = get('example.json')
.then(doSomething)
.then(doSomethingElse);

```
</br>

There are 4 stages in creating Promises:
1. Wrapping (syntax, or the Promise structure)
2. Thening (when it works)
3. Catching (recovery, when there's an error)
4. Chaining (where you create long sequences of asynchronous work)

And there are 4 states of Promises:
1. Fulfilled (it worked)
2. Rejected (failed)
3. Pending (still waiting)
4. Settled (something happened)

</br>

Promises execute in the main thread, meaning they are still potentially blocking.
```js
 new Promise(function (resolve, reject){
   resolve('hi') // works
   reject('bye') // can't happen a second time
})
```
Promises are like "try...catch" wrappers around asynchronous functions.

</br>

```js
new Promise(function (resolve, reject){
   const value = doSomething()
   if (thingWorked){
       resolve(value)
   } else if (somethingWentWrong) {
       reject()
   }
})
.then(function(value){
   //success
   return nextThing(value)
})
.catch(rejectFunction)

new Promise(function (resolve, reject){
   let img = document.createElement('img')
   img.src = src
   img.onload = resolve
   img.onerror = reject
   document.body.appendChild(img)
})
.then(finishLoading)
.catch(showAlternateImage)
```

</br>

For error handling there are two options.
Using a catch:
```js
get('example.json')
   .then(resolveFunc)
   .catch(rejectFunc)

```

Using a second .then to handle the error
```js
get('example.json')
   .then(resolveFunc)
   .then(undefined, rejectFunc)
```

Using a .catch is easier to read and write so it is the recommended option.
