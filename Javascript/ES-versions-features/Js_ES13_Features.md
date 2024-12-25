
# JavaScript ES13 Features

1. **Top-level Await** - Allows using await at the top level of modules.
```javascript
const response = await fetch('https://api.example.com/data');
const data = await response.json();
console.log(data);
```

2. **Array findLast and findLastIndex** - Finds the last matching element or index.
```javascript
const arr = [1, 2, 3, 2];
console.log(arr.findLast(x => x === 2)); // Outputs: 2
console.log(arr.findLastIndex(x => x === 2)); // Outputs: 3
```

3. **Hashbang (`#!`)** - Allows specifying interpreters in scripts.
```javascript
#!/usr/bin/env node
console.log('Hello from Node.js!');
```
