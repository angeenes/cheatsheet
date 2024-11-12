
# JavaScript Promises & Async/Await Cheatsheet

1. **Promise.resolve** - Creates a resolved promise.
```javascript
const promise = Promise.resolve('Done');
promise.then(value => console.log(value)); // Outputs: 'Done'
```

2. **Promise.reject** - Creates a rejected promise.
```javascript
const promise = Promise.reject('Error');
promise.catch(error => console.log(error)); // Outputs: 'Error'
```

3. **async/await** - Handles asynchronous operations.
```javascript
async function fetchData() {
  const response = await fetch('https://api.example.com/data');
  const data = await response.json();
  console.log(data);
}
```

4. **Promise.all** - Waits for all promises to resolve.
```javascript
const p1 = Promise.resolve(1);
const p2 = Promise.resolve(2);
Promise.all([p1, p2]).then(results => console.log(results)); // Outputs: [1, 2]
```

5. **Promise.allSettled** - Returns results of all promises, regardless of their state (fulfilled/rejected).
```javascript
const p1 = Promise.resolve(1);
const p2 = Promise.reject('Error');
Promise.allSettled([p1, p2]).then(results => console.log(results));
/* Outputs:
[
  { status: "fulfilled", value: 1 },
  { status: "rejected", reason: "Error" }
]
*/
```

6. **Promise.race** - Resolves/rejects as soon as the first promise settles.
```javascript
const p1 = new Promise(resolve => setTimeout(() => resolve('First'), 100));
const p2 = new Promise(resolve => setTimeout(() => resolve('Second'), 200));
Promise.race([p1, p2]).then(result => console.log(result)); // Outputs: 'First'
```

7. **Promise.any** - Resolves as soon as the first promise fulfills, ignoring rejections.
```javascript
const p1 = Promise.reject('Error');
const p2 = Promise.resolve('Success');
Promise.any([p1, p2]).then(result => console.log(result)); // Outputs: 'Success'
```

8. **Promise.then** - Executes when a promise resolves.
```javascript
Promise.resolve('Done').then(value => console.log(value)); // Outputs: 'Done'
```

9. **Promise.catch** - Handles promise rejections.
```javascript
Promise.reject('Error').catch(error => console.log(error)); // Outputs: 'Error'
```

10. **Promise.finally** - Executes code after a promise is settled (fulfilled or rejected).
```javascript
Promise.resolve('Done')
  .finally(() => console.log('Finally'))
  .then(value => console.log(value)); 
// Outputs: 'Finally', 'Done'
```
