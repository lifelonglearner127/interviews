Write a program to print all the LEADERS in the array.
An element is leader if it is greater than all the elements to its right side.
And the rightmost element is always a leader.

For example in the array {16, 17, 4, 3, 5, 2}, leaders are 17, 5 and 2. 
Let the input array be arr[] and size of the array be size.

```python
def find_solution(l):
    solution = []
    length = len(l)
    max_right = l[-1]
    solution.append(max_right)
    for i in range(length - 2, -1, -1):
        if l[i] > max_right:
            max_right = l[i]
            solution.append(max_right)
    return solution

assert set(find_solution([16, 17, 4, 3, 5, 2])) == {17, 5, 2}
```