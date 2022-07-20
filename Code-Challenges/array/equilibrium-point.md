Equilibrium index of an array is an index such that the sum of elements at lower indexes is equal to the sum of elements at higher indexes.

```
Input: A[] = {-7, 1, 5, 2, -4, 3, 0} 
Output: 3 
3 is an equilibrium index, because: 
A[0] + A[1] + A[2] = A[4] + A[5] + A[6]

Input: A[] = {1, 2, 3} 
Output: -1 
``` 

Solutions:
```python
def find_solution(l):
    total_sum = sum(l)
    left_sum = 0
    for i, element in enumerate(l):
        total_sum -= element
        if left_sum == total_sum:
            return i
        left_sum += element
    return -1

assert find_solution([-7, 1, 5, 2, -4, 3, 0]) == 3
assert find_solution([1, 2, 3]) == -1
```
Time Complexity: O(n)
Auxiliary Space: O(1)
