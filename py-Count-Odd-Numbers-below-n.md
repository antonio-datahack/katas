Given a number n, return the number of positive odd numbers below n, EASY!
Examples (Input -> Output)

7  -> 3 (because odd numbers below 7 are [1, 3, 5])
15 -> 7 (because odd numbers below 15 are [1, 3, 5, 7, 9, 11, 13])

Expect large Inputs!




```py
def odd_count(n):
    odds = [i for i in range(n) if i % 2 != 0 ]
    return len(odds)


def odd_count(n):
    odds = [num for num in range(1, n , 2)]
    return len(odds)
    
```
