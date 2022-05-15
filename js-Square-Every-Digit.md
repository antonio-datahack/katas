<h3>Instruction</h3>

Welcome. In this kata, you are asked to square every digit of a number and concatenate them.

For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.

Note: The function accepts an integer and returns an integer

**My Solution:**

```js
function squareDigits(num){
  let str = (num + "").split('');
  let numero = [];
  for (i of str) numero.push(i*i)
  return +numero.join("")
}


```

another solutions:


```js
function squareDigits(num){
  return Number(('' + num).split('').map(function (val) { return val * val;}).join(''));
  
}

function squareDigits(num){
  var array = num.toString().split('').map( function(int) {
    var i = parseInt(int);
    return i * i;
  });
  
  return parseInt(array.join(""));
}

function squareDigits(num){
  return +num.toString().split('').map(i => i*i).join('');
}

function squareDigits(num){
  let result = num
    .toString()
    .split("")
    .map( num => parseInt(num) )
    .map( num => num * num )
    .join("")
   
  return parseInt(result)
}

function squareDigits(num){
  return +String(num).split('').map(function(num){return +num * +num;}).join('');
}

const squareDigits = (num) => Number((num + '').split("").map(c => c *c).join(""));

squareDigits = n => Number(n.toString().split('').map(e => e * e).join(''));

function squareDigits(num){
  return +(num+'').split('').map(a=>a*a).join('');
}
