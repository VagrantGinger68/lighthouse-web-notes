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
Executes a provided function once for each array element.
```js
const array1 = [1,2,3]

array1.forEach((element) => {
  console.log(element) 
})

//1
//2
//3
```

## Filter
Creates a "shallow copy" of a portion of a given array, filtered down to just the elements from the given array that pass the test implemented by the provide function.
```js
const words = ['hello', 'world', 'coding', 'elephant', 'computer', 'pizza'];

const result = words.filter((word) => word.length > 6);

console.log(result);
//["elephant", "computer"]
```

## Reduce
Executes a user-provide "reducer" callback function on each element of an array, in order, passing in the return value from the calculation on the preceding element. The final result of running the reducer across all elements is a single value.
```js
const array1 = [1, 2, 3, 4];

// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce((accumulator, currentValue) => accumulator + currentValue, initialValue);

console.log(sumWithInitial);
//10
```

## Recursion (in loops)
A function taht calls itself until is satisfies an exit condition.
```js
function countDownFrom(number) {
	if (number === 0) {
		return;
	}
    console.log(number);    
    countDownFrom(number - 1);
}

countDownFrom(5);
```

## Recursive Case
The part where the function calls on itself.
```js
// function countDownFrom(number) {
	// if (number === 0) {
		// return;
	// }
    // console.log(number);    
    countDownFrom(number - 1);
// }

// countDownFrom(5);
```

## Base Case
The condition to stop the recursion.
```js
// function countDownFrom(number) {
	if (number === 0) {
		return;
	}
    // console.log(number);    
    // countDownFrom(number - 1);
// }

// countDownFrom(5);
```

## Iteration (in loops)
The process of repeating the same procedure multiple times.
For and While loops are examples of Iteration.

## Methods
A shorter syntax that defining a function property in an object. It can also be used in classes.
```js
const obj = {
  hello() {
    return 'world!';
  },
};

console.log(obj.hello());
//'world!'
```

## Arrow Function
A compact alternative to a traditional function expression.
```js
const arr = [1,2,3]
arr.forEach((num) => console.log(num));
```

## Async
Enables a program to start a potentially long-running task and still be able to be responsive to other tasks while that task runs, rather than needing to wait for that task to finish.

## Promises
Represents the eventual completion or failure of an asynchronous operation and its returning value.
```js
const executorFunction = (resolve, reject) => {
  if (someCondition) {
      resolve('I resolved!');
  } else {
      reject('I rejected!'); 
  }
}
const myFirstPromise = new Promise(executorFunction);
```

## TCP
A communications standard that enables applications and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks.

## HTTP
A protocol for fetching resources such as HTML documents. It is a client-side protocol so requests are initiated by the recipient (web browser). 

## JSON
JSON (JavaScript Object Notation) is a lightweight format for exchanging data between different systems and programming languages, commonly used in web APIs. It consists of key-value pairs.

## API
An application program interface (API) is a set of routines, protocols, and
tools for building software applications. an API specifies how software components should interact.
Additionally, APIs are used when programming graphical user interface (GUI)
components.

## Object Oriented Programming
a computer programming model that organizes software design around data, or objects, rather than functions and logic.

## Class
A template for creating objects. They contain data with code to work on that data. 
```js
// Declaration
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}

// Expression; the class is anonymous but assigned to a variable
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};

// Expression; the class has its own name
const Rectangle = class Rectangle2 {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
};
```

## Inheritance
To create a class inheritance, use the extends keyword.
```js
class Animal {
  constructor(name) {
    this.speed = 0;
    this.name = name;
  }
  run(speed) {
    this.speed = speed;
    alert(`${this.name} runs with speed ${this.speed}.`);
  }
  stop() {
    this.speed = 0;
    alert(`${this.name} stands still.`);
  }
}

class Rabbit extends Animal {
  hide() {
    alert(`${this.name} hides!`);
  }
}

let rabbit = new Rabbit("White Rabbit");
```

## Super
A keyword used to access properties on an object literal or class's [[Prototype]].
```js
class Rectangle {
  static logNbSides() {
    return "I have 4 sides";
  }
}

class Square extends Rectangle {
  static logDescription() {
    return `${super.logNbSides()} which are all equal`;
  }
}
Square.logDescription(); // 'I have 4 sides which are all equal'
```

## Express
Express is a minimal and flexible Node.js web application framework
that provides a robust set of features for web and mobile
applications.

## EJS
EJS or Embedded Javascript Templating is a templating engine used by Node.js. Template engine helps to create an HTML template with minimal code. Also, it can inject data into an HTML template on the client side and produce the final HTML.

## Cookies
A cookie is a piece of data from a website that is stored within a web browser that the website can retrieve at a later time. 

## Tree Data Structure
A tree is a data structure where a node can have zero or more children. Each node contains a value. The connection between nodes is called "edges". The structure starts with the "root" node and "branch" of with its descendants, down to its "leaves".
!["Tree structure image"](https://adrianmejia.com/images/tree-parts.jpg)