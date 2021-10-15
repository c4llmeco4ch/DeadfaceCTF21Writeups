# Unfinished

## Category

Programming

## Point Value

5 Points

## Prompt

There seems to be something wrong with this code. Can you figure out how to make it return the flag? Modify the code to show the flag. Submit the flag as: `flag{flag-goes-here}`.

```python
#!/usr/bin/env python3
from binascii import unhexlify as u

def get_flag():
    flag = '666c61677b30682d6c6f6f6b2d612d466c61477d'
    return u(flag).decode('utf-8')


print(f'The flag is: ')
```

## Solution

First, we run the program and are left with `The flag is:`. Clearly, there is an issue with the function, `get_flag()` not properly displaying its result in the print statement. The problem is our code never references the function elsewhere. Thus, while `get_flag()` provides a means to figure out the flag, we do not ever run the code inside it. To fix this, we simply need to add a call to `get_flag()` inside our print statement. But how?

The simplest way would be to concatenate the result of `get_flag()` with the current string: `print(f'The flag is: ' + get_flag())`. However, there is a cleaner way to use the tools already provided by the code. The 'f' before the quotes means this is [an f-string](https://www.geeksforgeeks.org/formatted-string-literals-f-strings-python/). As such, we can utilize the f-string's format to create a slightly more elegant solution:

```python
#!/usr/bin/env python3
from binascii import unhexlify as u

def get_flag():
    flag = '666c61677b30682d6c6f6f6b2d612d466c61477d'
    return u(flag).decode('utf-8')


print(f'The flag is: {get_flag()}')
```

Running this code provides us with the correct flag: `flag{0h-look-a-FlaG}`
