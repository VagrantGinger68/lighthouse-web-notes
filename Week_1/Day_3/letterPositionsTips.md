### Tips

1. Initialize an empty object to hold the results
```js
let results = {};
```

</br>

2. Make a for loop that goes through each letter of a sentence and makes sure its not a space (" "). If the letter is already in results and has multiple occurences, push the newly found location to results. If the letter isn't in results yet, make a new entry.
```js
for (let i = 0; i < sentence.length; i++) {
    if (sentence[i] !== " ") {
      if (results[sentence[i]]) {
        results[sentence[i]].push(i);
      } else {
        results[sentence[i]] = [i];
      }
    }
  }
```

</br>

3. return the results object
```js
return results
```

</br>

The full program should look like this:
```js
const letterPositions = function(sentence) {
  let results = {};

  for (let i = 0; i < sentence.length; i++) {
    if (sentence[i] !== " ") {
      if (results[sentence[i]]) {
        results[sentence[i]].push(i);
      } else {
        results[sentence[i]] = [i];
      }
    }
  }

  return results;
};
```