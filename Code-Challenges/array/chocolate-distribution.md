Given an array of n integers where each value represents the number of chocolates in a packet. Each packet can have a variable number of chocolates. There are m students, the task is to distribute chocolate packets such that: 

1. Each student gets one packet.
2. The difference between the number of chocolates in the packet with maximum chocolates and packet with minimum chocolates given to the students is minimum.

Please take a look at [here](https://www.geeksforgeeks.org/chocolate-distribution-problem/)

Examples:
```
Input : arr[] = {7, 3, 2, 4, 9, 12, 56} , m = 3 
Output: Minimum Difference is 2 
Explanation:
We have seven packets of chocolates and we need to pick three packets for 3 students 
If we pick 2, 3 and 4, we get the minimum difference between maximum and minimum packet sizes.

Input : arr[] = {3, 4, 1, 9, 56, 7, 9, 12} , m = 5 
Output: Minimum Difference is 6 
Explanation:
The set goes like 3,4,7,9,9 and the output is 9-3 = 6

Input : arr[] = {12, 4, 7, 9, 2, 23, 25, 41, 30, 40, 28, 42, 30, 44, 48, 43, 50} , m = 7 
Output: Minimum Difference is 10 
Explanation:
We need to pick 7 packets. We pick 40, 41, 42, 44, 48, 43 and 50 to minimize difference between maximum and minimum. 
```

Solutions:
```python
def find_solution(arr, m):
    length = len(arr)
    if m == 0 or length == 0:
        return 0
    if m > length:
        return -1
    arr.sort()
    min_diff = arr[-1] - arr[0]
    for i in range(length - m + 1):
        min_diff = min(min_diff, arr[i + m - 1] - arr[i])
    return min_diff

assert find_solution([7, 3, 2, 4, 9, 12, 56], 3) == 2
assert find_solution([3, 4, 1, 9, 56, 7, 9, 12], 5) == 6
assert find_solution([12, 4, 7, 9, 2, 23, 25, 41, 30, 40, 28, 42, 30, 44, 48, 43, 50], 7) == 10
```
