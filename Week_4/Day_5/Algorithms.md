## Algorithms

### Intro to Algoirthm Complexity

Algorithmic complexity is about how fast or slow a particular algorithm is. Different computers solve algorithms at different speeds so time isn't the best unit to measure the speed of an algorithm.

We calculate the speed of algorithms by counting the number of "elementary operations". The number of operations taht are so simple that they take a constant amount of time to perform.

Examples of elementary operations:

* let number = 0;
* number += 2;
* console.log(number);

We count all the elementary operations that an algorithm performs and call that its running time. If an algorithm performs "n" elementary operations, we say the running time is "n".

### Elementary Operations

An elementary operation is any operation that takes a fixed amount of time to perform, no matter what the data is.

If you have "number1 + number2", it only has 1 elementary operation (adding the numbers). It doesn't matter if its 1 + 2 or 500 + 1000;

```js
const array = [1, 2, 3, 4, 5]; 1 
let largest = 0; 1
for (let i = 0; 1
i < array.length; n + 1
i++ n) {
  const element = array[i]; n
  if (element > largest n) {
    largest = element; 1
  }
}
```

### Linear vs Logarithmic Algorithms

A linear search starts at 1 and continues until it reachs the desired result.

An example of binary search:
1. Let min = 1 and max = n.
2. Guess the average of max and min, rounded down so that it is an integer.
3. If you guessed the number, stop because you found it.
4. If the guess was too low, set min to be on larger than the guess.
5. If the guess whas too high, set max to be one smaller than the guess.
6. Go back to step two.

### Quadratic

Linear is more efficient compared to quadratic. Quadratic has to do (n^2 + n) / 2 amount of comparisons where linear only has to do n amount.

### Big O

Big O notation, written as O(), describes how the number of steps in an algorithm scales relative to its input. 

When we evaluate an algorithm using Big O notation, we only care about arbitrarily large input.

If our algorithm had a running time of n^0 + n^1 + n^2 + n^3 + n^4, it would simply be O(n^4).

When we evaluate an algorithm using Big O notation, we also drop the constants. Big O notation is used to describe how an algorithm's complexity grows relative to its input. It is not used to describe the exact running time of an algorithm.

* 2n + 3 will grow linearly, O(n)
* 100n^2 will grow exponentially, O(n^2)
* log n + 1000000000 will grow logarithmically, O(log n)

<br>

An algorithm that will always take the same amount of time to execute, no matter what the input is, runs in constant time.
Constant time algorithms run in O(1).
Example:
```js
array[1]

array[1] + array[2] + array[3]
```

When the number of operations an algorithm has to perform grows linearly relative to its input, then that algorithm runs in linear time.
Linear algorithms run in O(n).
Example:
```js
function sumAllNumberInArray(array) {
  let result = 0;

  for (let i = 0; i < array.length; i++) {
    let number = array[i];
    result += number;
  }

  return result;
}
```

If the number of operations that an algorithm has to perform is directly proportional to the square of the size of the input, then that algorithm runs in quadratic time.
Example:
```js
function arrayContainsSum(array, sum) {

  for (let i = 0; i < array.length; i++) {
    const element1 = array[i];

    for (let ii = 0; ii < array.length; ii++) {

      const element2 = array[ii];

      if (element1 + element2 === sum) {
        return true;
      }
    }
  }
  return false;
}
```

If the number of operations that an algorithm has to do is directly proportional to the logarithm of the size of the input, then that algorithm runs in logarithmic time. Logarithmic algorithms run in O(log n).
Example:
```js
function binarySearch(array, item) {
  let min = 0;
  let max = array.length - 1;

  while (true) {
    const middleIndex = Math.floor((min + max)/2.0);
    const currentItem = array[middleIndex];

    if (currentItem === item) {
      return middleIndex;
    } else if (currentItem < item) {
      min = middleIndex + 1;
    } else {
      max = middleIndex - 1;
    }

    if (min > max) {
      return null;
    }
  }
}
```