A permutation also called an "arrangement number" or "order", is text rearrangement of the elements of an ordered list S into text one-to-one correspondence with S itself. A string of length n has n! permutation. 
Take a look at [here](https://www.geeksforgeeks.org/write-a-c-program-to-print-all-permutations-of-a-given-string/)

Example:
```
Below are the permutations of string ABC. 
ABC ACB BAC BCA CBA CAB
```

Solution:
```python
def find_permutation(text, l, r):
    if l == r:
        print("".join(text))
    for i in range(l, r):
        text[i], text[l] = text[l], text[i]
        find_permutation(text, l + 1, r)
        text[i], text[l] = text[l], text[i]


text = list('ABC')
find_permutation(text, 0, 3)
```
