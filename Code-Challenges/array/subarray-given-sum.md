Given an unsorted array arr of nonnegative integers and an integer sum, find a continuous subarray which adds to a given sum. There may be more than one subarrays with sum as the given sum, print first such subarray. 

Examples : 
```
Input: arr[] = {1, 4, 20, 3, 10, 5}, sum = 33
Output: Sum found between indexes 2 and 4
Sum of elements between indices 2 and 4 is 20 + 3 + 10 = 33
```

Solutions:
```python
def find_solution(l, sum_):
    start = 0
    length = len(l)
    current_sum = l[0]
    i = 1
    while i <= length:
        while current_sum > sum_ and start < i - 1:
            current_sum -= l[start]
            start += 1
        if current_sum == sum_:
            return [start, i - 1]
        if i < length:
            current_sum += l[i]
        i += 1

assert find_solution([1, 4, 20, 3, 10, 5], 33) == [2, 4]
``` 