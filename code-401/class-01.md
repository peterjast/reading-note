# **Node Ecosystem, TDD, CI/CD**

[<=== Back to Table of Contents](https://peterjast.github.io/reading-notes/)

## Array.map()

The map method iterates over each element in an array, passes the value of the element into a function and returns a new array with the corresponding outputs. Each array object is passed into the same function and then returns the object that will exist at the same index in the new array. For each iteration, the object or value might change, but the index of the function's input is the same index of the function's output in the new array. The new array is the same length as the original.

An array is like a list of objects stored in a special data structure which we call an array. In an array list items can contain multiple values or lists within lists. The map method takes an array of objects, and then creates a new array of objects where each new object is the result of doing something to the value of each original object. The original object and the new corresponding object will be in the same place in both arrays. The order of the corresponding objects in the new array will be in the same order of the objects in the original array.

Maps each array element's value into a new array with the same changes applied to each element

Takes a list of things, performs the same action on each thing and makes a new list with the new things

## Array.reduce()

The reduce method takes a special function you define as an argument. This function is performed on each element of the array and the return of each iteration is added to a running total which is output after the function has been performed on all of the elements. The function you define takes four inputs: the first is a value that accumulates the return value of each iteration of your function, the second is the value of the element of the current iteration, then you have the index and the array essentially keeping track of the iterations and current value. The first arg stores its value with each iteration and the function you provide uses the value of the second argument, the current iteration, to change the accumulating value in whatever way you defined. After each element in the array has been been interated through, the accumulated value is returned. You can also pass a second argument to the reduce method, a value that intializes your functions first argument, the running total. By doing so, the first element of the array will be included as the first value your function is performed on, otherwise, it will be skipped and the function will begin with the second element as the first value.

## superagent()

Promise .then() syntax:

```javascript
superagent.get(`https://goodandbadstuff.com/api/good`).then(results => console.log(results.body)).catch(err => console.log(err.message));
```

async/await syntax

```javascript
const getGoodStuff = async() => {
    try{
        const results = await superagent.get(`https://goodandbadstuff.com/api/good`);
        console.log(results.body); 
    } catch(err){
        console.log(err.message);
    }
}
```

## Promises

I like to think of promises as exactly what they sound like. When an asynchronous function returns a promise, they are essentially making a promise to return a value eventually when they can. Since JS is single-threaded, sometimes an asynchronous function has to wait to return a value and by returning a promise, it is *promising* to eventually return a value. We make code wait until promises are fulfilled so that other code can continue to run. If we have multiple asynchronous functions waiting, we can chain promises using .then(). Promises have internal state of rejected, resolved or pending. We can also use the new keyword to create a new Promise object with resolve, reject callbacks. Rejected means something went wrong, resolved if it was successful and pending if neither has occured yet. To access the values of Promise objects, you should use .then(), .catch() or async/await with error handling.

## Are All Callback Functions Asynchronous?

No, not all callbacks are asynchronous. For instance, a lot of array methods such as array.map() use callbacks, but they are not asynchronous. When the .map method is invoked, the callback is invoked. Callbacks are not asynchronous by default, but are typically asynchronous when external resources are involved like a server, API or DB. This is because external resources can be unpredictable and asynchronous functions help with error handling and the flow of the application.

## Resources

[https://eloquentjavascript.net/](https://eloquentjavascript.net)
