
# 🚀 Object-Oriented Programming (OOP) in JavaScript

This README serves as a quick reference guide to core OOP concepts in JavaScript. Whether you're building scalable web apps or preparing for interviews, mastering these fundamentals will elevate your coding game.

---

## 📘 Topics Covered

### 1. 🧬 Prototypes
- JavaScript uses **prototypal inheritance**.
- Every object has an internal link to another object called its **prototype**.
- You can add methods to objects via their prototype:
  ```js
  function Person(name) {
    this.name = name;
  }

  Person.prototype.sayHello = function () {
    console.log(`Hello, I'm ${this.name}`);
  };

  const user = new Person("Bhanu");
  user.sayHello(); // Hello, I'm Bhanu

2. 🆕 The new Operator
- Used to create instances of objects from constructor functions or classes.
- It does 4 things:
- Creates a new empty object.
- Sets the prototype of the object.
- Binds this to the new object.
- Returns the object.

3. 🏗️ Constructors
- Special functions used to initialize new objects.
- Can be written using function syntax or ES6 class syntax.

4. 🧱 Classes
- Introduced in ES6 for cleaner syntax.
- Behind the scenes, still uses prototypes.
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

const dog = new Animal("Dog");
dog.speak(); // Dog makes a sound

5. 🧩 Keywords: extends and super
- extends: Used to create a subclass.
- super: Calls the constructor or methods of the parent class.

class Dog extends Animal {
  constructor(name, breed) {
    super(name); // Calls Animal's constructor
    this.breed = breed;
  }

  speak() {
    super.speak(); // Optional: Call parent method
    console.log(`${this.name} barks`);
  }
}

const labrador = new Dog("Rocky", "Labrador");
labrador.speak();

🧠 Pro Tip
Understanding OOP in JavaScript is key to mastering frameworks like React (which uses class components and hooks), and backend logic in Node.js. Practice by building small apps that use inheritance and prototypes.
