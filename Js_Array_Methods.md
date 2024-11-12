
# **JavaScript Array Methods Cheatsheet**

1. **map** - Transforms each element in the array based on a provided function.
```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // Outputs: [2, 4, 6]
```

2. **filter** - Creates a new array with elements that pass a test defined by a callback function.
```javascript
const numbers = [1, 2, 3, 4];
const evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // Outputs: [2, 4]
```

3. **reduce** - Reduces the array to a single value by applying a function to each element.
```javascript
const numbers = [1, 2, 3];
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // Outputs: 6
```

4. **forEach** - Executes a provided function once for each array element.
```javascript
const numbers = [1, 2, 3];
numbers.forEach(num => console.log(num));
// Outputs: 1, 2, 3
```

5. **find** - Returns the first element that satisfies the provided testing function.
```javascript
const numbers = [1, 2, 3];
const found = numbers.find(num => num > 2);
console.log(found); // Outputs: 3
```

6. **findIndex** - Returns the index of the first element that satisfies the testing function.
```javascript
const numbers = [1, 2, 3];
const index = numbers.findIndex(num => num > 2);
console.log(index); // Outputs: 2
```

7. **some** - Checks if at least one element passes the provided testing function.
```javascript
const numbers = [1, 2, 3];
const hasEven = numbers.some(num => num % 2 === 0);
console.log(hasEven); // Outputs: true
```

8. **every** - Checks if all elements pass the provided testing function.
```javascript
const numbers = [1, 2, 3];
const allPositive = numbers.every(num => num > 0);
console.log(allPositive); // Outputs: true
```

9. **slice** - Returns a shallow copy of a portion of the array.
```javascript
const numbers = [1, 2, 3, 4];
const sliced = numbers.slice(1, 3);
console.log(sliced); // Outputs: [2, 3]
```

10. **splice** - Adds or removes elements from an array.
```javascript
const numbers = [1, 2, 3, 4];
numbers.splice(1, 2, 'a', 'b');
console.log(numbers); // Outputs: [1, 'a', 'b', 4]
```

11. **concat** - Merges two or more arrays into one.
```javascript
const array1 = [1, 2];
const array2 = [3, 4];
const merged = array1.concat(array2);
console.log(merged); // Outputs: [1, 2, 3, 4]
```

12. **join** - Joins all elements of an array into a string with a specified separator.
```javascript
const numbers = [1, 2, 3];
const joined = numbers.join('-');
console.log(joined); // Outputs: "1-2-3"
```

13. **reverse** - Reverses the order of elements in the array.
```javascript
const numbers = [1, 2, 3];
numbers.reverse();
console.log(numbers); // Outputs: [3, 2, 1]
```

14. **sort** - Sorts the elements of an array in place.
```javascript
const numbers = [3, 1, 2];
numbers.sort((a, b) => a - b);
console.log(numbers); // Outputs: [1, 2, 3]
```

15. **flat** - Flattens a nested array up to a specified depth.
```javascript
const nested = [1, [2, [3]]];
const flattened = nested.flat(2);
console.log(flattened); // Outputs: [1, 2, 3]
```

16. **flatMap** - Maps each element using a mapping function and flattens the result.
```javascript
const numbers = [1, 2];
const mapped = numbers.flatMap(num => [num, num * 2]);
console.log(mapped); // Outputs: [1, 2, 2, 4]
```

17. **indexOf** - Returns the first index of a specified element, or -1 if not found.
```javascript
const numbers = [1, 2, 3];
const index = numbers.indexOf(2);
console.log(index); // Outputs: 1
```

18. **lastIndexOf** - Returns the last index of a specified element.
```javascript
const numbers = [1, 2, 3, 2];
const index = numbers.lastIndexOf(2);
console.log(index); // Outputs: 3
```

19. **includes** - Checks if an array includes a specified value.
```javascript
const numbers = [1, 2, 3];
const hasTwo = numbers.includes(2);
console.log(hasTwo); // Outputs: true
```

20. **fill** - Fills all elements of an array with a static value.
```javascript
const numbers = [1, 2, 3];
numbers.fill(0);
console.log(numbers); // Outputs: [0, 0, 0]
```

21. **copyWithin** - Copies a part of the array to another location in the same array.
```javascript
const numbers = [1, 2, 3, 4];
numbers.copyWithin(1, 2);
console.log(numbers); // Outputs: [1, 3, 4, 4]
```

22. **from** - Creates a new array from an iterable or array-like object.
```javascript
const array = Array.from('123');
console.log(array); // Outputs: ['1', '2', '3']
```

23. **of** - Creates a new array from the given arguments.
```javascript
const array = Array.of(1, 2, 3);
console.log(array); // Outputs: [1, 2, 3]
```

24. **isArray** - Checks if a value is an array.
```javascript
const isArray = Array.isArray([1, 2, 3]);
console.log(isArray); // Outputs: true
```
