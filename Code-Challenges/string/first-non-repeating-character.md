Given a string, find the first non-repeating character in it.

Example:
```
input = "GeeksforGeeks"
output = "f"

input = "GeeksQuiz"
output = "G"
```

Solution:
```python
from collections import Counter
def find_solution(s):
    counter = Counter(s)
    for letter in s:
        if counter[letter] == 1:
            return letter


assert find_solution("GeeksforGeeks") == "f"
assert find_solution("GeeksQuiz") == "G"
```