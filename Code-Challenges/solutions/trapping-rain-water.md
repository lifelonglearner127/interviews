Given n non-negative integers representing an elevation map where the width of each bar is 1, compute how much water it is able to trap after raining.

```
Example 1:
Input: arr[]   = [2, 1, 2]
Output: 1
Explanation:
x.x
xxx

Example 2:
Input: arr[]   = [3, 1, 2, 1, 4]
Output: 5
Explanation:
    x
x...x
x.x.x
xxxxx
```

Solutions:
```python
def get_water_amount(l):
    result = 0
    for i in range(1, len(l) - 1):
        left_water_level = max(l[0:i])
        right_water_level = max(l[i+1:])
        water_level = min(left_water_level, right_water_level)
        result += water_level - l[i]
    return result


assert get_water_amount([2, 1, 2]) == 1
assert get_water_amount([3, 1, 2, 1, 4]) == 5
```
