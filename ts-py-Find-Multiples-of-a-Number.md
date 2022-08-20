```ts
export function findMultiples(integer: number, limit: number): number[] {
  let arr: number[] = [];
  for (let i: number = 1; i <= limit; i++) {
    if (i * integer <= limit) {
      arr.push(i * integer)
    }
  }
  return arr
}
```

```py
def find_multiples(integer, limit):
    return [(i * integer) for i in range(1, limit +1 ) if (i* integer) <= limit]
```
