# asynchronous communication

### 🖤 async

- return : promise object

```javascript
async function f() {
  return Promise.resolve(value);
}
f.then(alert);
```

### 🖤 await

- wait until promise settles
- return : its result

```javascript
async function f() {
  let promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("promise done"), 1000);
  });
  let result = await promise; // wait until the promise resolves
  alert(result); // "promise done"
}
```

Ref) https://javascript.info/async-await
