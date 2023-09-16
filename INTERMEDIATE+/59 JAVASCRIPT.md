
---

### JavaScript Basics

- **JavaScript** is a versatile programming language used for adding interactivity to websites.

---

### Variables and Data Types

- Variables store data.
- Data types: numbers, strings, booleans, objects, arrays.

```javascript
let name = 'John';
let age = 30;
let isActive = true;
let person = { name: 'John', age: 30 };
let numbers = [1, 2, 3, 4];
```

---

### Functions

- Functions group code into reusable blocks.

```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

let message = greet('John');
console.log(message); // Output: Hello, John!
```

---

### Conditional Statements

- Execute different code based on conditions.

```javascript
let hour = 12;

if (hour < 12) {
    console.log('Good morning!');
} else if (hour < 18) {
    console.log('Good afternoon!');
} else {
    console.log('Good evening!');
}
```

---

### Loops

- Repeatedly execute code.

```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

---

### DOM Manipulation

- **DOM (Document Object Model)** represents the structure of a document.
- JavaScript can be used to interact with the DOM.

```javascript
document.getElementById('myElement').innerHTML = 'New Content';
```

---

### Event Handling

- Execute code in response to events (clicks, keypresses, etc.).

```javascript
document.getElementById('myButton').addEventListener('click', function() {
    alert('Button clicked!');
});
```

---

### Asynchronous JavaScript

- JavaScript is single-threaded, but it can handle asynchronous tasks using callbacks, promises, and async/await.

```javascript
function getData() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve('Data received!');
        }, 2000);
    });
}

async function fetchData() {
    try {
        const data = await getData();
        console.log(data);
    } catch (error) {
        console.error(error);
    }
}

fetchData();
```

---

### JSON (JavaScript Object Notation)

- A lightweight data interchange format.

```javascript
let person = {
    name: 'John',
    age: 30,
    isActive: true
};

let jsonPerson = JSON.stringify(person);
console.log(jsonPerson);
```

---

### Libraries and Frameworks

- JavaScript has many libraries and frameworks (e.g., React, Vue.js) to simplify development.

---

JavaScript is a powerful language that can be used for a wide range of tasks in web development. It's crucial for creating dynamic and interactive web applications. Understanding the basics of JavaScript is fundamental for any web developer.