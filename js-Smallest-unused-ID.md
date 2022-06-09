
```js 
function nextId(ids){
  ids = ids.sort((a, b) => a - b);
  ids = [...new Set(ids)]
  for (let i = 0; i < ids.length; i++)
    if (ids[i] !== i) {
      return i
    } if (Number(ids.slice(-1)) === ids.length -1) {
      return ids.length
    }
} 

``
