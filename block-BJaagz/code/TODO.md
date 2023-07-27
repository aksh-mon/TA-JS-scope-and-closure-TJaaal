1. Implement `forEach` array method using Array.reduce

- `forEach` accepts two parameter array and callback
- It does not return anything
- It should work exactly like array `forEach` method

```js
function forEach(arr, cb) {
  arr.reduce((_, cV, i, arr) => {
    cb(cV, i, arr);
    return null;
  }, null);
}

forEach(['Sam', 'Jon', 'Arya'], (name, i, arr) =>
  console.log(name + name, i, arr)
);
```

2. Implement `map` array method using Array.reduce

- `map` accepts two parameter array and callback
- It returns same size of array
- It should work exactly like array `map` method

```js
function map(arr,cb) {

return arr.reduce((result, cV, i, arr) => {
    result.push(cb(cV, i, arr));
    return result;
  }, []);
}

map(['Sam', 'Jon', 'Arya'], (name) => name + name); // ['SamSam', 'JonJon', 'AryaArya']

```

3. Implement `filter` array method using Array.reduce

- `filter` accepts two parameter array and callback
- It returns same size or smaller array
- It should work exactly like array `filter` method

```js
function filter(arr,cb) {
  return arr.reduce((result, cV, i, arr) => {
    if (cb(cV, i, arr)) {
      result.push(cV);
    }
    return result;
  }, []);

}
filter(['Sam', 'Jon', 'Arya'], (name) =>
  name.startsWith('S')
); // ['Sam']

```
