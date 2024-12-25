
# JavaScript Date Methods Cheatsheet

1. **getFullYear** - Gets the year of a date.
```javascript
const date = new Date();
console.log(date.getFullYear()); // Outputs: current year
```

2. **getMonth** - Gets the month of a date (0-11).
```javascript
const date = new Date();
console.log(date.getMonth()); // Outputs: 0 for January
```

3. **getDate** - Gets the day of the month.
```javascript
const date = new Date();
console.log(date.getDate()); // Outputs: current day
```

4. **getDay** - Gets the day of the week (0-6, where 0 is Sunday).
```javascript
const date = new Date();
console.log(date.getDay()); // Outputs: 0 for Sunday
```

5. **getHours** - Gets the hour (0-23).
```javascript
const date = new Date();
console.log(date.getHours()); // Outputs: current hour
```

6. **getMinutes** - Gets the minutes (0-59).
```javascript
const date = new Date();
console.log(date.getMinutes()); // Outputs: current minutes
```

7. **getSeconds** - Gets the seconds (0-59).
```javascript
const date = new Date();
console.log(date.getSeconds()); // Outputs: current seconds
```

8. **getMilliseconds** - Gets the milliseconds (0-999).
```javascript
const date = new Date();
console.log(date.getMilliseconds()); // Outputs: current milliseconds
```

9. **getTime** - Gets the timestamp (milliseconds since January 1, 1970).
```javascript
const date = new Date();
console.log(date.getTime()); // Outputs: timestamp
```

10. **setFullYear** - Sets the year of a date.
```javascript
const date = new Date();
date.setFullYear(2025);
console.log(date); // Outputs: modified date
```

11. **setMonth** - Sets the month of a date (0-11).
```javascript
const date = new Date();
date.setMonth(11); // December
console.log(date);
```

12. **setDate** - Sets the day of the month.
```javascript
const date = new Date();
date.setDate(15);
console.log(date);
```

13. **setHours** - Sets the hour.
```javascript
const date = new Date();
date.setHours(20);
console.log(date);
```

14. **toLocaleDateString** - Converts the date to a string in the local date format.
```javascript
const date = new Date();
console.log(date.toLocaleDateString()); // Outputs: 'MM/DD/YYYY' in the US
```

15. **toLocaleTimeString** - Converts the time to a string in the local time format.
```javascript
const date = new Date();
console.log(date.toLocaleTimeString()); // Outputs: 'HH:MM:SS AM/PM' in the US
```

16. **toISOString** - Converts the date to ISO 8601 format.
```javascript
const date = new Date();
console.log(date.toISOString()); // Outputs: 'YYYY-MM-DDTHH:mm:ss.sssZ'
```

17. **toUTCString** - Converts the date to a string in UTC format.
```javascript
const date = new Date();
console.log(date.toUTCString()); // Outputs: 'Day, DD Mon YYYY HH:MM:SS GMT'
```

18. **now** - Returns the current timestamp.
```javascript
console.log(Date.now()); // Outputs: current timestamp in milliseconds
```

19. **parse** - Parses a date string and returns the timestamp.
```javascript
const timestamp = Date.parse("2025-12-31T23:59:59Z");
console.log(timestamp); // Outputs: timestamp for the given date
```

20. **setTime** - Sets the date and time based on a timestamp.
```javascript
const date = new Date();
date.setTime(Date.now());
console.log(date); // Outputs: current date and time
```
