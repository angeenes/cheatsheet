
# JavaScript ES11 Features

1. **Nullish Coalescing Operator (`??`)** - Provides a default value for null/undefined.
```javascript
const value = null;
console.log(value ?? 'Default'); // Outputs: 'Default'
```

2. **Optional Chaining (`?.`)** - Safely access deeply nested properties.
```javascript
const user = { address: { city: 'New York' } };
console.log(user?.address?.city); // Outputs: 'New York'
console.log(user?.contact?.email); // Outputs: undefined
```

3. **BigInt** - Represents integers with arbitrary precision.
```javascript
const bigInt = 123456789012345678901234567890n;
console.log(bigInt + 1n); // Outputs: 123456789012345678901234567891n
```

4. **Promise.allSettled** - Waits for all promises to settle.
```javascript
const promises = [Promise.resolve(1), Promise.reject('Error')];
Promise.allSettled(promises).then(results => console.log(results));
/* Outputs:
[
  { status: "fulfilled", value: 1 },
  { status: "rejected", reason: "Error" }
]
*/
```
