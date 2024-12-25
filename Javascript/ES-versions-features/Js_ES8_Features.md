
# JavaScript ES8 Features

1. **Object.entries** - Converts an object into an array of key-value pairs.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.entries(obj)); // Outputs: [['a', 1], ['b', 2]]
```

2. **Object.values** - Converts an object into an array of its values.
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.values(obj)); // Outputs: [1, 2]
```

3. **String Padding (padStart and padEnd)** - Pads strings with specified characters.
```javascript
const str = '5';
console.log(str.padStart(3, '0')); // Outputs: '005'
console.log(str.padEnd(3, '0'));   // Outputs: '500'
```

4. **Async/Await** - Simplifies working with promises.
```javascript
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  console.log(data);
}
fetchData();
```
