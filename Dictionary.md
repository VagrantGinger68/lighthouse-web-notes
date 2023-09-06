# Dictionary

## console.log
Outputs a message to the console.
```js
console.log("Hello, World!")
```

## Variable
Containers for storing data. Data can be changed.
```js
let name = "Bob";
name = "Joe"
```

## Const
A variable whose data cannot be changed.
```js
const name = "Bob";
name ≠ "Joe"; //This will not work because name is constant
```

## Data Types
JavaScript has 6 Datatypes:
1. Numbers.
2. Strings.
3. Booleans.
4. null.
5. undefined.
6. Objects.

## Comparison Operators
1. == Equal to
2. === Equal value and equal type
3. != Not equal
4. !== not equal value or not equal type
5. ">" greater than
6. "<" less than
7. ">=" greater than or equal to
8. "<=" less than or equal to

## Logical Operators
1. && and
2. || or
3. ! not

## Turnary Operator
```js
variableName = (condition) ? valueIfTrue : valueIfFalse
```

## Array
A special variable that can hold more than one value.
```js
let names = ["Bob", "Joe", "Ryan"]
```

## For Loop
Repeats until a specified condition evalutes to false.
```js
for (let i = 0; i =< 5; i++) {
  console.log(i)
}
```

## For of Loop
Loop that operates on the values inside an iterable object like an array or string.
```js
for (const name of nameArray) {
  console.log(name)
}
```

## For in Loop
Loops over all enumerable string properties of an object.
```js
for (const name in nameObject) {
  console.log(`${name}: ${nameObject[name]}`)
}
```

## While Loop
Executes a specified statement as long as the test condition evalutes to true.
```js
let i = 0;

while (i < 5) {
  i++
}

console.log(i) //should return 5
```

## If-Else Statement
Executes a block of code if a specified condition is true.
```js
if (num < 10) {
  console.log("Number is less than 10")
} else {
  console.log("Number is more than 10")
}
```

## Objects
A standalone entity, with properties and type.
```js
const object = {
  a : 1,
  b : 2,
  c : 3
}
```

## Primitive Data Types
Built-in data types that are Immutable. The current value can't be modified.
1. Boolean 
2. null
3. undefined
4. Number
5. BigInt
6. String
7. Symbol

## High Order Functions
A function that accepts functions as perameters and/or returns a function.

## First Class Functions
Functions that are treated like other variables.
```js
const name = () => {
  console.log("Bob");
};
name(); // Invoke it using the variable
// Bob
```

## Function Parameter
The names that are defined in the function definion
```js
function printName(name) {
  console.log(name)
} //name is the parameter
```

## Function Argument
The real values passed to (and received by) the function.
```js
printName("Bob"); //"Bob" is the argument
```

## Map
Creates a new array with the results of call a function on every element in the calling array.
```js
const num = [1,2,3];

const numMultipliedByTwo = num.map ((number) => {number * 2});

console.log(numMultipliedByTwo)// [2,4,6]
```

## For Each

## Filter

## Reduce

## Recursion (in loops)

## Recursive Case

## Base Case

## Iteration (in loops)

## Methods

## Arrow Function

## JS Data Types

## Async

## Promises

## TCP

## HTTP

## JSON

## API

## Object Oriented Programming

## Class

## Inheritance

## Super

## Express

## EJS

## Cookies