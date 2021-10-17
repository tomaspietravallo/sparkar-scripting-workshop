# Practice test answer

## Prompt:

Write a script, where you:
- Store the following Array: `[0,1,2,3,4,5]`
- Create a function that increments each number in the array by one
- Call this function ten times

## Sample solution

**Note**:

- There are many ways to write code that does the same thing.

    - What you name your functions doesn't matter that much, if your function wasn't called `incrementArray`, don't worry in the slightest

    - A "right" answer would follow roughly the same logic, even if the code doesn't look exactly the same.

- Instead of comparing directly to the answer, check out the *[possible mistakes](#possible-mistakes)*, and make sure you can understand why code that looked like those answers wouldn't be considered "good"


```js

// Store the Array
let arr = [0, 1, 2, 3, 4, 5];

// Create a function that we can re-use somewhere else in the code
function incrementArray() {
  // Use a for loop to run a bit of code on every item of the array
  for (let index = 0; index < arr.length; index++) {
    // increment every item of the array
    arr[index] += 1;
  }
}

// Use another for loop to call the function ten times
for (let x = 0; x < 10; x++) {
  incrementArray();
}

```

## Possible mistakes

These don't necessarily mean the code would fail to execute, but that the problem wasn't approached correctly

### Not using a for loop on incrementArray
As you can see, this becomes hard to read and maintain (if we change the size of the array, we'd need to change our function too)

```js
function incrementArray() {
  arr[0] += 1;
  arr[1] += 1;
  arr[2] += 1;
  arr[3] += 1;
  arr[4] += 1;
  arr[5] += 1;
}
```

## Calling incrementArray ten times by typing it out

This also becomes hard to read and modify, using a loop makes it easier to modify later on, because if you want to call the function more/less times, you only need to change one value instead of modifying multiple lines of code

```js
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
incrementArray();
```