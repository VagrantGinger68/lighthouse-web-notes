### Tips

1. Make a function that takes in an object and a callback
```js
const findKey = function(object, callback)
```

</br>

2. Loop through the object to get the keys
```js
for (let keys of object)
```

</br>

3. If the callback returns true with the object key, return the key
```js
if (callback(object[key])) {
  return key;
}
```

</br>

4. If no key is found, return undefined
```js
return underfined;
```

</br>

The full function should look like this:
```js
const findKey = function(object, callback) {
  //Loop through object to get the keys
  for (let key in object) {
    //If the callback returns true with the object key, return the key
    if (callback(object[key])) {
      return key;
    }
  }
  //If no key is found, return undefined
  return undefined;
};
```