Subarrays are arrays inside another array which only contains contiguous elements.
Given an array of integers, the task is to find the maximum subarray sum possible of all the non-empty subarrays.
```
Example:
Input: [-3, -4, 5, -1, 2, -4, 6, -1]
Output: 8
Explanation: Subarray [5, -1, 2, -4, 6] is the max sum contiguous subarray with sum 8.

Input: [-2, 3, -1, 2]
Output: 4
Explanation: Subarray [3, -1, 2] is the max sum contiguous subarray with sum 4.
```

Solutions:
```python
def find_solution(l):
    max_sum = 0
    current_sum = 0
    for i in l:
        current_sum += i
        if current_sum > max_sum:
            max_sum = current_sum
        if current_sum < 0:
            current_sum = 0
    return max_sum


assert find_solution([-3, -4, 5, -1, 2, -4, 6, -1]) == 8
assert find_solution([-2, 3, -1, 2]) == 4
```