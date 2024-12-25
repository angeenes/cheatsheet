
# JavaScript ES9 Features

1. **Rest/Spread Properties for Objects** - Collect or spread properties from objects.
```javascript
const obj = { a: 1, b: 2, c: 3 };
const { a, ...rest } = obj;
console.log(a); // Outputs: 1
console.log(rest); // Outputs: { b: 2, c: 3 }
```

2. **Promise.finally** - Executes code after a promise is settled (fulfilled or rejected).
```javascript
Promise.resolve('Done')
  .finally(() => console.log('Cleanup'))
  .then(result => console.log(result)); 
// Outputs: 'Cleanup', 'Done'
```
