
# JavaScript DOM Manipulation Cheatsheet

1. **querySelector** - Selects the first element matching a CSS selector.
```javascript
const element = document.querySelector('.class');
console.log(element);
```

2. **querySelectorAll** - Selects all elements matching a CSS selector.
```javascript
const elements = document.querySelectorAll('.class');
elements.forEach(el => console.log(el));
```

3. **getElementById** - Selects an element by its ID.
```javascript
const element = document.getElementById('id');
console.log(element);
```

4. **getElementsByClassName** - Selects all elements with the specified class name.
```javascript
const elements = document.getElementsByClassName('class');
console.log(elements); // Outputs: HTMLCollection
```

5. **getElementsByTagName** - Selects all elements with the specified tag name.
```javascript
const elements = document.getElementsByTagName('div');
console.log(elements); // Outputs: HTMLCollection
```

6. **textContent** - Gets or sets the text content of an element.
```javascript
const element = document.querySelector('.class');
console.log(element.textContent); // Outputs: text inside the element
element.textContent = 'New Text';
```

7. **innerHTML** - Gets or sets the HTML content of an element.
```javascript
const element = document.querySelector('.class');
console.log(element.innerHTML); // Outputs: HTML inside the element
element.innerHTML = '<span>New HTML</span>';
```

8. **style** - Gets or sets the CSS styles of an element.
```javascript
const element = document.querySelector('.class');
element.style.color = 'red';
element.style.fontSize = '20px';
```

9. **classList** - Adds, removes, or toggles classes on an element.
```javascript
const element = document.querySelector('.class');
element.classList.add('new-class');
element.classList.remove('old-class');
element.classList.toggle('active');
console.log(element.classList.contains('active')); // Outputs: true or false
```

10. **addEventListener** - Adds an event listener to an element.
```javascript
const button = document.querySelector('button');
button.addEventListener('click', () => console.log('Button clicked!'));
```

11. **removeEventListener** - Removes an event listener from an element.
```javascript
const button = document.querySelector('button');
const handleClick = () => console.log('Button clicked!');
button.addEventListener('click', handleClick);
button.removeEventListener('click', handleClick);
```

12. **appendChild** - Appends a child element to a parent.
```javascript
const parent = document.querySelector('.parent');
const child = document.createElement('div');
child.textContent = 'New Child';
parent.appendChild(child);
```

13. **removeChild** - Removes a child element from a parent.
```javascript
const parent = document.querySelector('.parent');
const child = parent.querySelector('.child');
parent.removeChild(child);
```

14. **createElement** - Creates a new HTML element.
```javascript
const element = document.createElement('div');
element.textContent = 'New Element';
document.body.appendChild(element);
```

15. **setAttribute / getAttribute** - Sets or gets an attribute of an element.
```javascript
const element = document.querySelector('.class');
element.setAttribute('data-info', 'Some Info');
console.log(element.getAttribute('data-info')); // Outputs: 'Some Info'
```

16. **removeAttribute** - Removes an attribute from an element.
```javascript
const element = document.querySelector('.class');
element.removeAttribute('data-info');
```

17. **parentNode** - Gets the parent node of an element.
```javascript
const child = document.querySelector('.child');
console.log(child.parentNode); // Outputs: parent element
```

18. **children** - Gets the child elements of an element.
```javascript
const parent = document.querySelector('.parent');
console.log(parent.children); // Outputs: HTMLCollection of child elements
```

19. **cloneNode** - Creates a copy of a node.
```javascript
const original = document.querySelector('.original');
const clone = original.cloneNode(true); // true copies all descendants
document.body.appendChild(clone);
```

20. **contains** - Checks if an element contains another element.
```javascript
const parent = document.querySelector('.parent');
const child = document.querySelector('.child');
console.log(parent.contains(child)); // Outputs: true or false
```
