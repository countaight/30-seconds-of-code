---
title: removeNullFromObject
tags: object,null,intermediate
---

Remove keys with a value of `null` from an object.

- Use `Object.entries()` in combination with `Array.prototype.reduce()` to create a new object with keys whose values aren't `null`

```js
const removeNullFromObject = obj =>
  {
    return Object.entries(obj).reduce((acc, [key, value]) => value === null ? acc : (acc[key] = value, acc), {});
  }
```

```js
const obj = { foo: 'bar', bar: null }
removeNullFromObject(obj); // { foo: 'bar' }
```
