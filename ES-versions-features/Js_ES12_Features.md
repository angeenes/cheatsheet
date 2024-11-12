
# JavaScript ES12 Features

1. **Logical Assignment Operators** - Combines logical operations with assignment.
```javascript
let a = null;
a ||= 'default';
console.log(a); // Outputs: 'default'

let b = 1;
b &&= 2;
console.log(b); // Outputs: 2
```

2. **Numeric Separators** - Improves readability of large numbers.
```javascript
const num = 1_000_000;
console.log(num); // Outputs: 1000000
```

3. **Replace All in Strings** - Replaces all occurrences of a substring.
```javascript
const str = 'foo foo foo';
console.log(str.replaceAll('foo', 'bar')); // Outputs: 'bar bar bar'
```

4. **Promise.any** - Resolves as soon as the first promise fulfills.
```javascript
const promises = [Promise.reject('Error'), Promise.resolve('Success')];
Promise.any(promises).then(result => console.log(result)); // Outputs: 'Success'
```
