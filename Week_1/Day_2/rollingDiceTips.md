### Tips

1. Use process.argv to gather the command line arguments that are passed into the program.

```js
let rolls = process.argv.slice(2);
```

</br>

2. Initialize an empty array to hold the results.
```js
let results = [];
```

</br>

3. Make a function that takes in one command line argument and assign that value to the amount of dice that are going to be rolled. Get a random number from 1-6 to represent each side of the dice. Then join the results with array.join(", "); Lastly log the results to the console.
```js
const diceRoller = function(rolls) {
  for (let i = 0; i < rolls; i++) {
    results.push(Math.floor(Math.random() * 6 + 1));
  }
  return results.join(", ");
};

console.log(`Rolled ${rolls} dice: ${diceRoller(rolls)}`);
```

</br>

The entire program together should look like this:
```js
let rolls = process.argv.slice(2);
let results = [];

const diceRoller = function(rolls) {
  for (let i = 0; i < rolls; i++) {
    results.push(Math.floor(Math.random() * 6 + 1));
  }
  return results.join(", ");
};

console.log(`Rolled ${rolls} dice: ${diceRoller(rolls)}`);
```