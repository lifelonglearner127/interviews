You are given a list of n-1 integers and these integers are in the range of 1 to n.
There are no duplicates in the list.
One of the integers is missing from the list. Write an efficient code to find the missing integer.

```
Example: 
Input: arr[] = {1, 2, 4, 6, 3, 7, 8}
Output: 5
Explanation: The missing number between 1 to 8 is 5

Input: arr[] = {1, 2, 3, 5}
Output: 4
Explanation: The missing number between 1 to 5 is 4
```

Solution:
```python
def find_solution(l):
    length = len(l)
    total_sum = (length + 1) * (length + 2) // 2
    return total_sum - sum(l)

assert find_solution([1, 2, 4, 6, 3, 7, 8]) == 5
```