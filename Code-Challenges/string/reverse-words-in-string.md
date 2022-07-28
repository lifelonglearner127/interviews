Let the input string be “i like this program very much”. The function should change the string to “much very program this like i”

```shell
Examples:
Input: s = “geeks quiz practice code” 
Output: s = “code practice quiz geeks”

Input: s = “getting good at coding needs a lot of practice” 
Output: s = “practice of lot a needs coding at good getting” 
```

Method 1:
```python
def find_solution(s):
    words = s.split()
    return " ".join(words[::-1])


assert find_solution("geeks quiz practice code") == "code practice quiz geeks"
assert find_solution("getting good at coding needs a lot of practice") == "practice of lot a needs coding at good getting"
```

Method 2:
```python
```


Method 1:
```javascript

```
