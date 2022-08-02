Given an array and a number k where k is smaller than the size of the array, we need to find the k’th smallest element in the given array. It is given that all array elements are distinct.

Please take a look at [here](https://www.geeksforgeeks.org/kth-smallestlargest-element-unsorted-array/)

Examples:
```
Input: arr[] = {7, 10, 4, 3, 20, 15}, k = 3 
Output: 7

Input: arr[] = {7, 10, 4, 3, 20, 15}, k = 4 
Output: 10 
```

Solution:
```python
def find_solution(arr, k):
    arr.sort()
    return arr[k - 1]

assert find_solution([7, 10, 4, 3, 20, 15], 3) == 7
assert find_solution([7, 10, 4, 3, 20, 15], 4) == 10
```
