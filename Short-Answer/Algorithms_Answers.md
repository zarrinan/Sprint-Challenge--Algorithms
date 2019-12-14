#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a)
```python
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```

The runtime complexity of the code above is O(n)


```
b)  sum = 0
    for i in range(n):
      j = 1
      while j < n:
        j *= 2
        sum += 1
```
The runtime complexity of the code above is O(n), since value of j is constant in outer `for` loop.

```
c)  def bunnyEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```
The recursive function calls itself n times, complexity is O(n)

## Exercise II

If want to minimize the number of eggs dropped and broken, the strategy would be starting from the floor 1 and going up drop the egg from each floor except the last. The first time the egg breaks f == floor #. This process consumes 1 egg. If the egg never breaks on all floors tested and it is a fact that an egg is broken at some floor then f == last floor. This process consumes no eggs.
This is an O(n/2) or O(n) runtime process.


If we want to minimize time to find the lowest floor where an egg gets broken, we should implement binary search strategy.
t = total number of floors. If egg is not broken at all floors, then f floor is the last floor, so the algorithm will check from 1 to t-1 floors.
Start at (t-1)/2 floor to see if egg gets broken, if it does, go to floor (t-1)/4; if it doesn't, go to floor (t-1)3/4; continue until there are 2 floors distance to check left and on one of the floors an egg gets broken and on another it doesn't.
This is a O(logn) runtime process.

