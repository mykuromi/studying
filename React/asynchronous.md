# Asynchronous communication

### 🖤 async

- return : promise object

```javascript
async function f() {
  return Promise.resolve(value);
}
f.then(alert);
```

### 🖤 await

- suspends the function execution until the promise settles and then resumes it with the promise result (JavaScript engine can do other jobs in the meantime: execute other scripts, handle events, etc.)
- return : its result
- can’t use in regular functions

```javascript
async function f() {
  let promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("promise done"), 1000);
  });
  let result = await promise; // wait until the promise resolves
  alert(result); // "promise done" in 1 sec
}
```

### 🖤 promise
- the eventual completion (or failure) of an asynchronous operation and its resulting value
- states : pending(initial state) / fulfilled / rejected

### 🖤 examples

```javascript
let response = await fetch('/article/promise-chaining/user.json');
let user = await response.json();
console.log(user);
```

Ref) https://javascript.info/async-await /
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise 
