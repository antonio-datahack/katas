
Prime Factors

Inspired by one of Uncle Bob's TDD Kata

Write a function that generates factors for a given number.

The function takes an integer on the standard input and returns a list of integers (ObjC: array of NSNumbers representing integers). That list contains the prime factors in numerical sequence.



```js
function prime_factors(n) {
  let arr = []
  for (let i = 2; i <= n; i++) {
    if (n % i === 0 ) {
      arr.push(i) 
      n = n/i
      i = 1
    }
  }
  return arr
}
```
