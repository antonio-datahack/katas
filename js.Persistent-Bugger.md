

Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

For example (Input --> Output):

39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit)
999 --> 4 (because 9*9*9 = 729, 7*2*9 = 126, 1*2*6 = 12, and finally 1*2 = 2)
4 --> 0 (because 4 is already a one-digit number)



```js
function suma(num) {
  let sum = 1
  let arr = num.toString().split("")
  for (let n of arr) {
    sum = sum * n   
}
  return sum
}

function persistence(num) {
   if (num.toString().length === 1) {
     return 0
   } else {
     let subtotal = suma(num)
     let counter = 1
     while (subtotal.toString().length > 1) {
       counter++
       subtotal = suma(subtotal)
     } 
      return counter 
   }
 }
 
 ///////////////////////////////////////////////////////
 
 function persistence(num) {
   let counter = 0;
  while(num.toString().length > 1){
    counter++
    num = num.toString().split("").map(Number).reduce((a, b) => a*b)
  }
  return counter
}
 ```
 
