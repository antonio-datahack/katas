https://www.codewars.com/kata/59df2f8f08c6cec835000012/train/javascript


```js
function meeting(s) {
  let nameUpper = s.toUpperCase().replace(/:/g, ", ").split(";");
  let fullName = nameUpper.map(name => "(" + name.slice(name.indexOf(" ") +1) + ", " + name.slice(0, name.indexOf(" ") -1) + ")").sort()
  return fullName.join().replace(/,/g, "").replace(/ /g, ", ")
}
```
