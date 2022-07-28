Given an array A[] consisting only 0s, 1s and 2s. The task is to write a function that sorts the given array. The functions should put all 0s first, then all 1s and all 2s in last.

This problem is also the same as the famous “Dutch National Flag problem”. The problem was proposed by Edsger Dijkstra. The problem is as follows:

Examples:
```
Input: {0, 1, 2, 0, 1, 2}
Output: {0, 0, 1, 1, 2, 2}

Input: {0, 1, 1, 0, 1, 2, 1, 2, 0, 0, 0, 1}
Output: {0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 2, 2}
```

```python
def sort012(l):
    length = len(l)
    li = 0
    mi = 0
    ri = length - 1
    while mi <= ri:
        if l[mi] == 0:
            l[li], l[mi] = l[mi], l[li]
            li += 1
            mi += 1
        elif l[mi] == 1:
            mi += 1
        else:
            l[mi], l[ri] = l[ri], l[mi]
            ri -= 1
    return l

assert sort012([0, 1, 2, 0, 1, 2]) == [0, 0, 1, 1, 2, 2]
assert sort012([0, 1, 1, 0, 1, 2, 1, 2, 0, 0, 0, 1]) == [0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 2, 2]
```
