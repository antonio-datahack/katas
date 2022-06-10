Your task is to sum the differences between consecutive pairs in the array in descending order.
Example

[2, 1, 10]  -->  9

In descending order: [10, 2, 1]

Sum: (10 - 2) + (2 - 1) = 8 + 1 = 9

If the array is empty or the array has only one element the result should be 0 (Nothing in Haskell, None in Rust).

**my solutions:**

```js

function sumOfDifferences(arr) {
let newArr = arr.sort((a, b) => a - b).reverse();
let sum = 0;
  for (let i = 0; i < newArr.length -1; i++) {
    sum += newArr[i] - newArr[i+1]
   }
  return sum
}

function sumOfDifferences(arr) {
let newArr = arr.sort((a, b) => b - a);
let sum = 0;
  for (let i = 0; i < newArr.length -1; i++) {
    sum += newArr[i] - newArr[i+1]
   }
  return sum
}

function sumOfDifferences(arr) {
  return arr.length > 1 ? Math.max(...arr) - Math.min(...arr) : 0
}

```
 
another solutions:

```js 

sumOfDifferences = arr => arr.length <= 1 ? 0 : Math.max(...arr) - Math.min(...arr);

const sumOfDifferences = arr =>
  arr.sort((a, b) => b - a).shift() - arr.pop() || 0;
  
const sumOfDifferences = a => a.length > 1 ? Math.max(...a) - Math.min(...a) : 0

```
