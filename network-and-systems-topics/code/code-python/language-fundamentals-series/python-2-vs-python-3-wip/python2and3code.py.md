---
description: >-
  This snippet of code has been tested to work on Python 2 and Python 3 by
  employing the techniques detailed in the blog post "Python 2 vs Python 3".
---

# Python2and3code.py

This snippet of code has been tested to work on Python 2 and Python 3 by employing the techniques detailed in the blog post "[Python 2 vs Python 3](./)".

```python
from __future__ import absolute_import, division, print_function
from pip._vendor.distlib.compat import raw_input


def get_input(prompt=''):
    try:
        line = raw_input(prompt)
    except NameError:
        x = input(prompt)
    return line


x = get_input('Type : ')

print(x)
```

