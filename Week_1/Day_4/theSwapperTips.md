### Tips

1. Make a function that takes in key1, object1, key2, and object2
```js
const swapper = function(key1, object1, key2, object2)
```

</br>

2. Gather keys stored in both objects
```js
const object1Value = object1[key1];
const object2Value = object2[key2];
```

</br>

3. Store the value of key2 in the place of key1 and vice versa.
```js
object1[key1] = object2Value;
object2[key2] = object1Value;
```

</br>

4. Log the swapped objects to the console.
```js
console.log("object1: ", object1);
console.log("object2: ", object2);
```

</br>

The full function should look like this:
```js
const swapper = function(key1, object1, key2, object2) {
  console.log("Swap!");

  //fetch keys stored in both objects
  const object1Value = object1[key1];
  const object2Value = object2[key2];

  //Store the value of key2 in place of key1
  object1[key1] = object2Value;
  object2[key2] = object1Value;

  console.log("object1: ", object1);
  console.log("object2: ", object2);
};
```