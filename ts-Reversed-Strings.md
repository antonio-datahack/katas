<pre>
Complete the solution so that it reverses the string passed into it.

'world'  =>  'dlrow'
'word'   =>  'drow'

</pre>

```ts
export function solution(str: string): string {
  return (str).split("").reverse().join(""); // reverse this!
}
```
