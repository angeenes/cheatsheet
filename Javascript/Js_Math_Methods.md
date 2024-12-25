
# JavaScript Math Methods Cheatsheet

1. **Math.abs** - Returns the absolute value of a number.
```javascript
console.log(Math.abs(-5)); // Outputs: 5
console.log(Math.abs(5));  // Outputs: 5
```

2. **Math.round** - Rounds a number to the nearest integer.
```javascript
console.log(Math.round(4.5)); // Outputs: 5
console.log(Math.round(4.4)); // Outputs: 4
```

3. **Math.floor** - Rounds a number down to the nearest integer.
```javascript
console.log(Math.floor(4.9)); // Outputs: 4
```

4. **Math.ceil** - Rounds a number up to the nearest integer.
```javascript
console.log(Math.ceil(4.1)); // Outputs: 5
```

5. **Math.max** - Returns the largest number from the inputs.
```javascript
console.log(Math.max(1, 3, 2)); // Outputs: 3
```

6. **Math.min** - Returns the smallest number from the inputs.
```javascript
console.log(Math.min(1, 3, 2)); // Outputs: 1
```

7. **Math.random** - Generates a random number between 0 (inclusive) and 1 (exclusive).
```javascript
console.log(Math.random()); // Outputs: a random number, e.g., 0.584
```

8. **Math.sqrt** - Returns the square root of a number.
```javascript
console.log(Math.sqrt(16)); // Outputs: 4
```

9. **Math.pow** - Raises a number to the power of another number.
```javascript
console.log(Math.pow(2, 3)); // Outputs: 8 (2^3)
```

10. **Math.trunc** - Removes the fractional part of a number.
```javascript
console.log(Math.trunc(4.9)); // Outputs: 4
console.log(Math.trunc(-4.9)); // Outputs: -4
```

11. **Math.sign** - Returns the sign of a number: 1 (positive), -1 (negative), or 0.
```javascript
console.log(Math.sign(-5)); // Outputs: -1
console.log(Math.sign(0));  // Outputs: 0
console.log(Math.sign(5));  // Outputs: 1
```

12. **Math.cbrt** - Returns the cube root of a number.
```javascript
console.log(Math.cbrt(27)); // Outputs: 3
```

13. **Math.log** - Returns the natural logarithm (base e) of a number.
```javascript
console.log(Math.log(1)); // Outputs: 0
console.log(Math.log(Math.E)); // Outputs: 1
```

14. **Math.log10** - Returns the base-10 logarithm of a number.
```javascript
console.log(Math.log10(100)); // Outputs: 2
```

15. **Math.log2** - Returns the base-2 logarithm of a number.
```javascript
console.log(Math.log2(8)); // Outputs: 3
```

16. **Math.exp** - Returns e^x, where x is the argument.
```javascript
console.log(Math.exp(1)); // Outputs: 2.718281828459045 (approximately e)
```

17. **Math.hypot** - Returns the square root of the sum of squares of its arguments.
```javascript
console.log(Math.hypot(3, 4)); // Outputs: 5 (Pythagorean theorem)
```

18. **Math.sin / cos / tan** - Returns the sine, cosine, or tangent of a number (in radians).
```javascript
console.log(Math.sin(Math.PI / 2)); // Outputs: 1
console.log(Math.cos(Math.PI));     // Outputs: -1
console.log(Math.tan(0));           // Outputs: 0
```

19. **Math.asin / acos / atan** - Returns the arcsine, arccosine, or arctangent of a number.
```javascript
console.log(Math.asin(1)); // Outputs: 1.5707963267948966 (PI/2)
console.log(Math.acos(0)); // Outputs: 1.5707963267948966 (PI/2)
console.log(Math.atan(1)); // Outputs: 0.7853981633974483 (PI/4)
```

20. **Math.atan2** - Returns the arctangent of the quotient of its arguments.
```javascript
console.log(Math.atan2(1, 1)); // Outputs: 0.7853981633974483 (PI/4)
```
