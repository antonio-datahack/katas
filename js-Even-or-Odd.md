**my solution:**

```js

function even_or_odd(number) {
  return number % 2 === 0 ? 'Even' : 'Odd'
}

// ------------------------------------------

function even_or_odd(number) {
  if (number % 2 === 0) return 'Even'
  return 'Odd'
}

```

**another solutions:**


```js

const even_or_odd = n => (n % 2) ? 'Odd' : 'Even';

```
