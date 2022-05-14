<h3>Introduction</h3>
Usually when you buy something, you're asked whether your credit card number, phone number or answer to your most secret question is still correct. However, since someone could look over your shoulder, you don't want that shown on your screen. Instead, we mask it.

Your task is to write a function maskify, which changes all but the last four characters into '#'.

Example:
```js
"4556364607935616" --> "############5616"
     "64607935616" -->      "#######5616"
               "1" -->                "1"
                "" -->                 ""

// "What was the name of your first pet?"

"Skippy" --> "##ippy"

"Nananananananananananananananana Batman!"
-->
"####################################man!"

```

My solution:

```js
function maskify(cc) {
    const str = cc + '';
    const last = str.slice(-4);
    return last.padStart(str.length, '#')
}
```

Nice Solutions:
```js
unction maskify(cc) {
  return cc.slice(0, -4).replace(/./g, '#') + cc.slice(-4);
}

function maskify(cc) {
  return cc.replace(/.(?=....)/g, '#');
}

maskify = (cc) => '#'.repeat(Math.max(0, cc.length - 4)) + cc.substr(-4);

const maskify = cc => cc.slice(-4).padStart(cc.length, '#')

```
