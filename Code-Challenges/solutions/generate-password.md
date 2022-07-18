Create Random Password with special characters, letters, digits.


```python
import random
import string
def generate_password(length=10):
    password = []
    uppercase_count = 2
    digits_count = 1
    special_character_count = 1    
    # generate upper case
    password.extend(
        random.choice(string.ascii_uppercase) for _ in range(uppercase_count)
    )
    # generate digits
    password.extend(
        random.choice(string.digits) for _ in range(digits_count)
    )
    # generate special letters
    password.extend(
        random.choice(string.punctuation) for _ in range(special_character_count)
    )
    # generate other letters
    password.extend(
        random.choice(string.ascii_letters + string.digits + string.punctuation)
        for _ in range(length - uppercase_count - digits_count - special_character_count)
    )
    random.shuffle(password)
    return ''.join(password)

```