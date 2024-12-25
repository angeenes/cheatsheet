
# JavaScript Object Methods Cheatsheet

1. **Object.keys** - Returns an array of an object's keys.
```javascript
const obj = { a: 1, b: 2, c: 3 };
console.log(Object.keys(obj)); // Outputs: ['a', 'b', 'c']
```

2. **Object.values** - Returns an array of an object's values.
```javascript
const obj = { a: 1, b: 2, c: 3 };
console.log(Object.values(obj)); // Outputs: [1, 2, 3]
```

3. **Object.entries** - Returns an array of key-value pairs.
```javascript
const obj = { a: 1, b: 2, c: 3 };
console.log(Object.entries(obj)); // Outputs: [['a', 1], ['b', 2], ['c', 3]]
```

4. **Object.assign** - Copies properties from one or more source objects to a target object.
```javascript
const target = { a: 1 };
const source = { b: 2, c: 3 };
Object.assign(target, source);
console.log(target); // Outputs: { a: 1, b: 2, c: 3 }
```

5. **Object.freeze** - Makes an object immutable (cannot be changed).
```javascript
const obj = { a: 1 };
Object.freeze(obj);
obj.a = 2; // This will not change the value
console.log(obj); // Outputs: { a: 1 }
```

6. **Object.seal** - Allows modifying existing properties but prevents adding or removing properties.
```javascript
const obj = { a: 1 };
Object.seal(obj);
obj.b = 2; // This will not add a new property
console.log(obj); // Outputs: { a: 1 }
```

7. **Object.hasOwn** - Checks if an object has a specified property as its own (not inherited).
```javascript
const obj = { a: 1 };
console.log(Object.hasOwn(obj, 'a')); // Outputs: true
console.log(Object.hasOwn(obj, 'b')); // Outputs: false
```

8. **Object.create** - Creates a new object with the specified prototype.
```javascript
const proto = { greet: function() { return 'Hello'; } };
const obj = Object.create(proto);
console.log(obj.greet()); // Outputs: 'Hello'
```

9. **Object.fromEntries** - Converts an array of key-value pairs into an object.
```javascript
const entries = [['a', 1], ['b', 2]];
const obj = Object.fromEntries(entries);
console.log(obj); // Outputs: { a: 1, b: 2 }
```
