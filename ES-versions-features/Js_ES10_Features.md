
# JavaScript ES10 Features

1. **Array.prototype.flat** - Flattens nested arrays up to a specified depth.
```javascript
const nested = [1, [2, [3, [4]]]];
console.log(nested.flat(2)); // Outputs: [1, 2, 3, [4]]
```

2. **Array.prototype.flatMap** - Maps each element and then flattens the result.
```javascript
const numbers = [1, 2];
console.log(numbers.flatMap(x => [x, x * 2])); // Outputs: [1, 2, 2, 4]
```

3. **Optional Catch Binding** - Allows omitting the error parameter in catch blocks.
```javascript
try {
  throw new Error('Oops');
} catch {
  console.log('Error handled');
}
```
