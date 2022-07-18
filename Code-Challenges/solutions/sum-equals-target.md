Find a pair of elements (indices of the two numbers) from a given array whose sum equals a specific target number.

```python
def find_indices(l, target):
    lookup = {}
    for i, n in enumerate(l):
        if target - n in lookup:
            return lookup[target - n], i
        else:
            lookup[n] = i

assert set(find_indices([1, 2, 3, 4], 7)) == {3, 2}
```
