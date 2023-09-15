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

### Linear vs Logarithmic Algorithms

A linear search starts at 1 and continues until it reachs the desired result.

An example of binary search:
1. Let min = 1 and max = n.
2. Guess the average of max and min, rounded down so that it is an integer.
3. If you guessed the number, stop because you found it.
4. If the guess was too low, set min to be on larger than the guess.
5. If the guess whas too high, set max to be one smaller than the guess.
6. Go back to step two.

