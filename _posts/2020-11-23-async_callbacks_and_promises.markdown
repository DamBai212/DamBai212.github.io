---
layout: post
title:      "Async, Callbacks, & Promises"
date:       2020-11-23 21:56:12 +0000
permalink:  async_callbacks_and_promises
---


**Synchronous vs Asynchronous**
Synchronous means the execution happens in a single event. It will only execute the next task once the previous task is finished.
In Asynchronous, the execution will never wait to complete, instead, it will execute all the events in a single go and multiple events will be in progress, hence making JavaScript non-blocking. Task 2 will be performed even if task 1 isn’t finished.

```
// Synchronous code
const result = database.query("SELECT * FROM users");
console.log("query executed");
console.log("run another query");


// Asynchronous  code
database.query("SELECT * FROM users", function(result) {
    console.log("Query finished");
});
console.log("run another query");
```

Synchronous code (Blocking) — In the above example, the code will run sequentially and all the steps will be completed synchronously.
Asynchronous code (Non-Blocking) — The next code in the sequence will run and it won’t be blocked by the previous one.

**Callback**
The callback function is a function that will get called after the execution of the first function and it will run the second function.
A function that can be passed as an argument to the higher-order functions and can return function. The argument passed as a function to the higher-order function is called a callback.

**Promises**
A promise is an object which keeps track of whether the asynchronous event has happened already or not and determines what happens after the event has occurred.
Instead of providing a callback, a promise has its own methods (resolved or rejected), which you call to tell the promise what will happen when it is successful or when it fails.
It can be in three states, fulfilled, pending, or rejected. It helps to catch all the errors that occurred after rejection or attach a callback to the handle of the fulfilled value.
