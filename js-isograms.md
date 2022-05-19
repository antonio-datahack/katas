<h2>Introduction</h2>

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

Example: (Input --> Output)

```
"Dermatoglyphics" --> true
"aba" --> false
"moOse" --> false (ignore letter case)
```
my solutions:

```js

function isIsogram(str){
  let newWord = new Set(str.toUpperCase());
  return [...newWord].length === [...str].length ? true : false
}

function isIsogram(str){
  return new Set(str.toUpperCase()).size === str.length;
}

```

another solutions:



```js

function isIsogram(str){
  return new Set(str.toUpperCase()).size == str.length;
}

function isIsogram(str){ 
  return !/(\w).*\1/i.test(str)
}

function isIsogram(str){
  return !str.match(/([a-z]).*\1/i);
}

function isIsogram (str) {
  return !str || (str.length === new Set(str.toLowerCase()).size);
}

```  
