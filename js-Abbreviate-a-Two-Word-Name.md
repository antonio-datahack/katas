Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot separating them.

It should look like this:

Sam Harris => S.H

patrick feeney => P.F

my solutions: 
```js

function abbrevName(name){
  return name.slice(0,1).toUpperCase() +"."+ name.slice(name.indexOf(' ') +1, name.indexOf(' ')+2).toUpperCase()
}

function abbrevName(name){
  return name[0].toUpperCase() +"."+ name[name.indexOf(' ') +1].toUpperCase()
}

```


another solutions: 

```js

function abbrevName(name){
    return name.split(' ').map(i => i[0].toUpperCase()).join('.')
}

const abbrevName = name => name.match(/\b\w/g).join('.').toUpperCase()

abbrevName = n => n.replace(/(.).* (.).*/, '$1.$2').toUpperCase()

```
