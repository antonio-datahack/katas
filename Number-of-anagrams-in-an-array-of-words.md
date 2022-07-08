![link to exercise](https://www.codewars.com/kata/587e18b97a25e865530000d8/train/javascript)

An anagram is a word, a phrase, or a sentence formed from another by rearranging its letters. An example of this is "angel", which is an anagram of "glean".

Write a function that receives an array of words, and returns the total number of distinct pairs of anagramic words inside it.

Some examples:

    There are 2 anagrams in the array ["dell", "ledl", "abc", "cba"]
    There are 7 anagrams in the array ["dell", "ledl", "abc", "cba", "bca", "bac"]




```js
function anagramCounter (wordsArray) {
  let sorted = wordsArray.map(word => word.split("").sort().join("").toLowerCase())
  let counter = 0
  for (let word of sorted) {
    --counter
    for (let w of sorted) {
      if (w === word) {
        ++counter
      }
    }
    
  }
  return counter/2;
}
```
