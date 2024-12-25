
# JavaScript Regular Expressions (Regex) Cheatsheet

1. **.test** - Tests if a pattern matches a string.
```javascript
const regex = /hello/i;
console.log(regex.test('Hello World')); // Outputs: true
console.log(regex.test('Goodbye World')); // Outputs: false
```

2. **.exec** - Executes a search for a match and returns the result.
```javascript
const regex = /hello/;
const match = regex.exec('hello world');
console.log(match[0]); // Outputs: 'hello'
console.log(match.index); // Outputs: 0
```

3. **Modifiers** - `g`, `i`, `m` (global, case-insensitive, multiline).
```javascript
const regexGlobal = /hello/g;
console.log('hello hello'.match(regexGlobal)); // Outputs: ['hello', 'hello']

const regexCaseInsensitive = /hello/i;
console.log(regexCaseInsensitive.test('Hello')); // Outputs: true

const regexMultiline = /^hello/m;
console.log(regexMultiline.test('hello
world')); // Outputs: true
```

4. **Character Classes** - `\d`, `\w`, `\s`, and more.
```javascript
const regexDigits = /\d+/;
console.log('abc123'.match(regexDigits)); // Outputs: ['123']

const regexWordCharacters = /\w+/;
console.log('hello_world!'.match(regexWordCharacters)); // Outputs: ['hello_world']

const regexWhitespace = /\s+/;
console.log('hello world'.match(regexWhitespace)); // Outputs: [' ']
```

5. **Quantifiers** - `*`, `+`, `?`, `{n,m}` (zero or more, one or more, optional, range).
```javascript
const regexZeroOrMore = /a*/;
console.log('aaab'.match(regexZeroOrMore)); // Outputs: ['aaa']

const regexOneOrMore = /a+/;
console.log('aaab'.match(regexOneOrMore)); // Outputs: ['aaa']

const regexOptional = /colou?r/;
console.log('color'.match(regexOptional)); // Outputs: ['color']
console.log('colour'.match(regexOptional)); // Outputs: ['colour']

const regexRange = /a{2,4}/;
console.log('aaaab'.match(regexRange)); // Outputs: ['aaa']
```

6. **Anchors** - `^`, `$` (start, end of string).
```javascript
const regexStart = /^hello/;
console.log(regexStart.test('hello world')); // Outputs: true
console.log(regexStart.test('world hello')); // Outputs: false

const regexEnd = /world$/;
console.log(regexEnd.test('hello world')); // Outputs: true
console.log(regexEnd.test('world hello')); // Outputs: false
```

7. **Groups and Backreferences** - `()`, `(?:)`, `\n`.
```javascript
const regexGroup = /(hello) (world)/;
const match = 'hello world'.match(regexGroup);
console.log(match[0]); // Outputs: 'hello world'
console.log(match[1]); // Outputs: 'hello'
console.log(match[2]); // Outputs: 'world'

const regexNonCapturingGroup = /(?:hello) world/;
console.log(regexNonCapturingGroup.test('hello world')); // Outputs: true
```

8. **Alternation** - `|` (logical OR).
```javascript
const regexOr = /cat|dog/;
console.log('I have a cat'.match(regexOr)); // Outputs: ['cat']
console.log('I have a dog'.match(regexOr)); // Outputs: ['dog']
```

9. **Lookahead and Lookbehind** - `(?=)`, `(?!)`, `(?<=)`, `(?<!)`.
```javascript
const regexPositiveLookahead = /hello(?= world)/;
console.log(regexPositiveLookahead.test('hello world')); // Outputs: true
console.log(regexPositiveLookahead.test('hello there')); // Outputs: false

const regexNegativeLookahead = /hello(?! world)/;
console.log(regexNegativeLookahead.test('hello world')); // Outputs: false
console.log(regexNegativeLookahead.test('hello there')); // Outputs: true

const regexPositiveLookbehind = /(?<=hello )world/;
console.log(regexPositiveLookbehind.test('hello world')); // Outputs: true

const regexNegativeLookbehind = /(?<!hello )world/;
console.log(regexNegativeLookbehind.test('hello world')); // Outputs: false
console.log(regexNegativeLookbehind.test('goodbye world')); // Outputs: true
```

10. **Escape Sequences** - Escaping special characters like `.` or `*`.
```javascript
const regexEscape = /a\.b/;
console.log('a.b'.match(regexEscape)); // Outputs: ['a.b']
console.log('acb'.match(regexEscape)); // Outputs: null
```
