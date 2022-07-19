Given a string s containing just the characters '(', ')', '{', '}', '[', and ']', determine if the input string is valid or not.

Note that an input string is valid if:
- Open brackets must be closed by the same type of brackets
- Open brackets must be closed in the correct order

```python
def is_valid(s):
    stack = []
    opening_brackets = set('({[')
    closing_brackets = set(')}]')
    pair = {'}': '{', ')': '(', ']': '['}
    for i in s:
        if i in opening_brackets:
            stack.append(i)
        if i in closing_brackets:
            if not stack:
                return False
            elif stack.pop() != pair[i]:
                return False
            else:
                continue 
    if not stack:
        return True
    else:
        return False

assert is_valid('(){}[]') is True
assert is_valid('(({[]}))') is True
assert is_valid('()}[]') is False
```
