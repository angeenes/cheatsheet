
# JavaScript ES15 Features (ECMAScript 2024)

ES15 introduces the following confirmed features:

1. **Array Grouping by Key** - Groups elements in an array based on a callback function.
```javascript
const items = [{ category: 'fruit', name: 'apple' }, { category: 'fruit', name: 'banana' }, { category: 'vegetable', name: 'carrot' }];
const grouped = items.groupBy(item => item.category);
console.log(grouped);
// Outputs:
// {
//   fruit: [{ category: 'fruit', name: 'apple' }, { category: 'fruit', name: 'banana' }],
//   vegetable: [{ category: 'vegetable', name: 'carrot' }]
// }
```

2. **Symbol Metadata** - Enhanced metadata capabilities using symbols.
```javascript
const metaSymbol = Symbol.metadata;
class Example {
  static [metaSymbol] = { createdBy: 'John Doe', version: 1.0 };
}
console.log(Example[metaSymbol]); // Outputs: { createdBy: 'John Doe', version: 1.0 }
```

3. **Improved Top-Level Await** - Enhancements to error handling with top-level await.
```javascript
try {
  const data = await fetch('https://api.example.com');
  console.log(await data.json());
} catch (error) {
  console.error('Error fetching data:', error);
}
```

For more detailed information on ES15 features, refer to the [ECMAScript 2024 Specification](https://tc39.es/ecma262/).
