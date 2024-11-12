
# JavaScript ES6+ Features Cheatsheet

1. **let / const** - Block-scoped variable declarations.
```javascript
let a = 5;
const b = 10;
console.log(a, b); // Outputs: 5, 10
```

2. **Arrow Functions** - Shorter function syntax.
```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // Outputs: 5
```

3. **Template Literals** - Embeds variables into strings.
```javascript
const name = "John";
console.log(`Hello, ${name}!`); // Outputs: 'Hello, John!'
```

4. **Destructuring** - Extracts data from arrays/objects.
```javascript
const [a, b] = [1, 2];
console.log(a, b); // Outputs: 1, 2

const { x, y } = { x: 10, y: 20 };
console.log(x, y); // Outputs: 10, 20
```

5. **Default Parameters** - Sets default values for function parameters.
```javascript
function greet(name = "Guest") {
  return `Hello, ${name}`;
}
console.log(greet()); // Outputs: 'Hello, Guest'
```

6. **Rest Operator** - Collects all remaining arguments into an array.
```javascript
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3, 4)); // Outputs: 10
```

7. **Spread Operator** - Spreads elements of an array/object.
```javascript
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // Outputs: [1, 2, 3, 4]

const obj1 = { a: 1 };
const obj2 = { ...obj1, b: 2 };
console.log(obj2); // Outputs: { a: 1, b: 2 }
```

8. **Classes** - Simplified syntax for creating objects.
```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    return `Hello, ${this.name}`;
  }
}
const john = new Person("John");
console.log(john.greet()); // Outputs: 'Hello, John'
```

9. **Modules (import/export)** - Organizes code into separate files.
```javascript
// math.js
export const add = (a, b) => a + b;

// main.js
import { add } from './math.js';
console.log(add(2, 3)); // Outputs: 5
```

10. **Promises** - Handles asynchronous operations.
```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Done"), 1000);
});
promise.then(result => console.log(result)); // Outputs: 'Done'
```

11. **Async/Await** - Simplifies working with promises.
```javascript
async function fetchData() {
  const response = await fetch("https://api.example.com/data");
  const data = await response.json();
  console.log(data);
}
fetchData();
```

12. **Map/Set** - New data structures for unique values or key-value pairs.
```javascript
const set = new Set([1, 2, 2, 3]);
console.log(set); // Outputs: Set { 1, 2, 3 }

const map = new Map();
map.set('a', 1);
console.log(map.get('a')); // Outputs: 1
```

13. **Symbols** - Creates unique identifiers.
```javascript
const sym = Symbol('unique');
console.log(sym); // Outputs: Symbol(unique)
```

14. **Optional Chaining (?.)** - Safely access deeply nested properties.
```javascript
const user = { address: { city: "New York" } };
console.log(user?.address?.city); // Outputs: 'New York'
console.log(user?.contact?.email); // Outputs: undefined
```

15. **Nullish Coalescing Operator (??)** - Provides a default value for null/undefined.
```javascript
const value = null;
console.log(value ?? "Default"); // Outputs: 'Default'
```

16. **for...of** - Iterates over iterable objects.
```javascript
const arr = [1, 2, 3];
for (const num of arr) {
  console.log(num); // Outputs: 1, 2, 3
}
```
