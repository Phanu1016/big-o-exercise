# Big O Exercise

## Step One:

### O(n + 10)

Answer: O(n)

### O(100 * n)
Answer: O(n)

### O(25)
Answer: O(1)

### O(n^2 + n^3)
Answer: O(n^3)

### O(n + n + n + n)
Answer: O(n)

### O(1000 * log(n) + n)
Answer: O(n)

### O(1000 * n * log(n) + n)
Answer: O(n log(n))

### O(2^n)
Answer: O(n^2)

### O(5 + 3 + 1)
Answer: O(1)

### O(n + n^(1/2) + n^2 + n * log(n)^10)
Answer: O(n + n^1/2)


## Step Two:

```js
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```
Answer: O(n)

```js
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```
Answer: O(n)

```js
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```
Answer: O(1)

```js
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
```
Answer: O(n)

```js
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
```
Answer: O(n^2)

```js
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```
Answer: O(n)

## Step Three:
### True or false: n^2 + n is O(n^2).
Answer: True
### True or false: n^2 * n is O(n^3).
Answer: True
### True or false: n^2 + n is O(n).
Answer: False
### What’s the time complexity of the .indexOf array method?
Answer: O(n)
### What’s the time complexity of the .includes array method?
Answer: O(n)
### What’s the time complexity of the .forEach array method?
Answer: O(n)
### What’s the time complexity of the .sort array method?
Answer: O(n log n)
### What’s the time complexity of the .unshift array method?
Answer: O(n)
### What’s the time complexity of the .push array method?
Answer: O(1)
### What’s the time complexity of the .splice array method?
Answer: O(n)
### What’s the time complexity of the .pop array method?
Answer: O(1)
### What’s the time complexity of the Object.keys() function?
Answer: O(n)