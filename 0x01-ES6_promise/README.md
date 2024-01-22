## 0x01. ES6 Promises

### Description:

Promises in JavaScript are a mechanism for handling asynchronous operations. They represent a value that may be available now, or in the future, or possibly never. Promises have three states:

1. `Pending:`The initial state, the promise is still being processed.

2. `Fulfilled:` The asynchronous operation completed successfully, and the promise now has a resulting value.

3. `Rejected:` The asynchronous operation failed, and the promise has a reason for the failure.

Promises provide a cleaner way to structure asynchronous code compared to traditional callbacks. They allow you to chain operations together, handle errors more effectively, and avoid "callback hell." Promises have methods like `.then()` for handling fulfillment and `.catch()` for handling rejection.

Example:
```
const myPromise = new Promise((resolve, reject) => {
  // Asynchronous operation, e.g., fetching data
  const success = true;

  if (success) {
    resolve("Operation successful");
  } else {
    reject("Operation failed");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.error(error);
  });
```
This is a simple example, but Promises become particularly powerful when dealing with complex asynchronous code, such as making multiple asynchronous calls in sequence or in parallel. Additionally, modern JavaScript now includes async/await, built on top of Promises, which further simplifies asynchronous code.
