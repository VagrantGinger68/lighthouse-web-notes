## Object Oriented Programming

### Summary

A big part of Object Oriented programming is to give a plan for modularity. When programming in an object oriented way, we use objects to keep our code modular and reduce repetition.

</br>

In object oriented programming, we use objects to group related variables and functions together to keep our code more organized. 
```js
const dog = {
  sound: "woof",
  dogBreed: "shih tzu",
  speak: function() {
    console.log(`${this.dogBreed} says ${this.dogSound}`);
  }
};
```
When a property's value is a function, it is called a method.

</br>

For object oriented programming we use the "this" keyword. The value of "this" is determined at the time of the call and depends on how and where it was called. "this" refers to the object that the method was called on.

## Classes

Classes are blueprints. We use them to created instances of obejects. A class describes what the object is going to be and we can create new objects with the class.

Example class:
```js
class Pizza {

  constructor() {
    this.toppings = ["cheese"];
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }

}
```
The constructor holds all the default options that we want each object to have. Then we can add other methods as well. Values can also be passed into the constructor.

Example:
```js
class Pizza {

  constructor(size, crust) {
    this.size = size;
    this.crust = crust;
    this.toppings = ["cheese"];
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }

}

let pizza = new Pizza('large', 'thin');
```

Example of using the class and its methods:
```js
let pizza1 = new Pizza();
console.log(pizza1.toppings); // ["cheese"]
pizza1.addTopping("mushrooms");
pizza1.addTopping("peppers");
console.log(pizza1.toppings); // ["cheese", "mushrooms", "peppers"]

let pizza2 = new Pizza();
console.log(pizza2.toppings); // ["cheese"]
pizza2.addTopping("more cheese");
console.log(pizza2.toppings); // ["cheese", "more cheese"];
```

</br>

## Inheritance

Inheritance can be used to reduce duplicated code between similar objects.

Example without Inheritance:
```js
class Student {
  // this constructor is identical to that of a mentor!
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  // here is a method that is specific to students
  enroll(cohort) {
    this.cohort = cohort;
  }

  // identical! Smells of code duplication
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}

class Mentor {
  // this constructor is identical to that of a student!
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  // specific to mentors
  goOnShift() {
    this.onShift = true;
  }

  // specific to mentors
  goOffShift() {
    this.onShift = false;
  }

  // identical! Smells of code duplication
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}
```

Example with inheritance:
```js
// This class represents all that is common between Student and Mentor
class Person {
  // moved here b/c it was identical
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  // moved here b/c it was identical
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}

class Student extends Person {
  // stays in Student class since it's specific to students only
  enroll(cohort) {
    this.cohort = cohort;
  }
}

class Mentor extends Person {
  // specific to mentors
  goOnShift() {
    this.onShift = true;
  }

  // specific to mentors
  goOffShift() {
    this.onShift = false;
  }
}
```

We make a new Person class with all the things that were the same between Student and Mentor, then we can extend Person into other classes to add specific methods. Student and Mentor are subclasses of the Person class.

</br>

## Super

Methods can be overridden in subclasses to change their behavior. We can use "super" to help prevent duplicate code. 

Example:
```js
// Super class
class Person {
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}

class Mentor extends Person {
  // Mentor bios need to include a bit more info
  bio() {
    return `I'm a mentor at Lighthouse Labs. ${super.bio()}`;
  }
}

// DRIVER CODE

const bob = new Mentor('Bob Ross', 'I like mountains way too much');
console.log(bob.bio());
```

</br>

## Getters and Setters

Getters and Setters are special methods that are used to get the value of a property or set the value of a property.

The main reasons to use these are:
1. Validating data before assigning it a property.
2. Computing a value on the fly instead of simply pulling it out of the property.

Example :
```js
class Pizza {

  get price() {
    const basePrice = 10;
    const toppingPrice = 2;
    return basePrice + this.toppings.length * toppingPrice;
  }

  set size(size) {
    if (size === 's' || size === 'm' || size === 'l') {
      this._size = size;
    }
  }
}

let pizza = new Pizza();

pizza.price;      // instead of getPrice()
pizza.size = 's'; // instead of setSize(size)
```

</br>

Another example of inheritance:

Without Inheritance:
```js
class Flower {
  water() {
    console.log("Watering the flower");
    this.lastWatered = Date();
  }
}

class Tree {
  water() {
    console.log("Watering the tree");
    this.lastWatered = Date();
  }
}

class Bush {
  water() {
    console.log("Watering the bush");
    this.lastWatered = Date();
  }
}
```

With Inheritance:
```js
class Plant {
  water() {
    console.log(`Watering the ${this.type}`);
    this.lastWatered = Date();
  }
}

class Flower extends Plant {
  constructor() {
    super()
    this.type = "flower";
  }
}

class Tree extends Plant {
  constructor() {
    super()
    this.type = "tree";
  }
}

class Bush extends Plant {
  constructor() {
    super()
    this.type = "bush";
  }
}
```