---
description: >-
  How to overcome some of the differences between major versions with the use of
  __future__
---

# Python 2 vs Python 3

[Full Source video](https://www.youtube.com/watch?v=h5AQeMhYTfU)

[Introduction Video to the full series](https://www.youtube.com/watch?time_continue=205&v=eiYemtNKS-M&feature=emb_logo) 

## print

#### **In Python 2:** 

print is a _statement_

![](../../../../.gitbook/assets/image%20%2833%29.png)

**In Python 3:** 

print is a _function_

![Functions need parenthesis around the arguments we&apos;re passing them](../../../../.gitbook/assets/image%20%2831%29.png)

**In Python 2:** 

If we were to wrap our string in parenthesis it would print without issues... **But**...

![It would also print without issues... But..](../../../../.gitbook/assets/image%20%2834%29.png)

### Why?

Because 'hello' in **Python 2** would be a **tuple** of a single object.

### What is a tuple?

Collection or two \(2\) or more objects. Tuples are represented by using parenthesis around the objects that comprise them.

**In Python 2:** will just convert this back to a string

![It converts it to a string because it is a single object tuple](../../../../.gitbook/assets/image%20%2836%29.png)

If we were to add a second object, it would be kept as a tuple after hitting enter

![This time the tuple was not transformed to a string](../../../../.gitbook/assets/image%20%2841%29.png)

This is not the behavior that would be observed **In Python 3**:

![In Python 3 print is a function and needs to have arguments passed in \(\)](../../../../.gitbook/assets/image%20%2840%29.png)

Since print is a **function in Python 3**, the arguments would be passed to print\(\) function and they would be printed as expected

![print is a function in Python 3 and arguments are passed to print\(\)](../../../../.gitbook/assets/image%20%2845%29.png)

If we want our scripts to run i**n Python 2** and i**n Python 3**, we would want _common operations_ such as print to run in both versions. 

## How to write Python scripts that run on Python 2 and Python 3?

### Importing futures

A solution to the problem stated above is given by the use of futures. "futures" make Python 2 behave like Python 3 for certain functions. 

#### [From the Python 3 docs - \_\_future\_\_ — Future statement definitions: ](https://docs.python.org/3/library/__future__.html)

| feature | optional in | mandatory  | effect |
| :--- | :--- | :--- | :--- |
| nested\_scopes | 2.1.0b1 | 2.2 | [**PEP 227**](https://www.python.org/dev/peps/pep-0227): _Statically Nested Scopes_ |
| generators | 2.2.0a1 | 2.3 | [**PEP 255**](https://www.python.org/dev/peps/pep-0255): _Simple Generators_ |
| division | 2.2.0a2 | 3.0 | [**PEP 238**](https://www.python.org/dev/peps/pep-0238): _Changing the Division Operator_ |
| absolute\_import | 2.5.0a1 | 3.0 | [**PEP 328**](https://www.python.org/dev/peps/pep-0328): _Imports: Multi-Line and Absolute/Relative_ |
| with\_statement | 2.5.0a1 | 2.6 | [**PEP 343**](https://www.python.org/dev/peps/pep-0343): _The “with” Statement_ |
| print\_function | 2.6.0a2 | 3.0 | [**PEP 3105**](https://www.python.org/dev/peps/pep-3105): _Make print a function_ |
| unicode\_literals | 2.6.0a2 | 3.0 | [**PEP 3112**](https://www.python.org/dev/peps/pep-3112): _Bytes literals in Python 3000_ |
| generator\_stop | 3.5.0b1 | 3.7 | [**PEP 479**](https://www.python.org/dev/peps/pep-0479): _StopIteration handling inside generators_ |
| annotations | 3.7.0b1 | 4.0 | [**PEP 563**](https://www.python.org/dev/peps/pep-0563): _Postponed evaluation of annotations_ |

In this case _**print** is_ 

### **print\_function**:

First, we import it from \_\_future\_\_:

`from __future__ import print_function`

![print function behaves like in Python 3](../../../../.gitbook/assets/image%20%2848%29.png)

Now if after importing print\_function from \_\_future\_\_ we attempted to use the print function, it will never behave like a statement again which is the **native Python 2 behavior**

![Just as in Python 3, print&quot;hello&quot;, errors out. See below](../../../../.gitbook/assets/image%20%2854%29.png)

![](../../../../.gitbook/assets/image%20%2857%29.png)

**In Python 3:** if we were to import print\_function from [\_\_future\_\_](https://docs.python.org/3/library/__future__.html)

_from \_\_future\_\_ import print\_function_ it would just ignore it. 

![](../../../../.gitbook/assets/image%20%2844%29.png)

Nothing changes in the behavior of Python 3 by importing the print function from \__\_future\_\__

## Division

In Python 2, floor division drops the remainder and returns only a whole number.

![](../../../../.gitbook/assets/image%20%2843%29.png)

Python 2 thinks that you are dividing an integer by an integer, and that you probably want and integer back and drops the remainder.

If, instead, we were to provide one of the numbers as a float, the returned result would be a float too.

![A floating point number aka &quot;float&quot;, is a number that includes decimal portion.](../../../../.gitbook/assets/image%20%2842%29.png)

Again, if we wanted to have Python 2 behave like Python 3, we may import the **division \_\_future\_\_** module

![We import division from \_\_future\_\_](../../../../.gitbook/assets/image%20%2855%29.png)

After importing the **division** module from **\_\_future\_\_** and performing a division that would yield a remainder we can observe that **Python 2** is outputting the expected remainder

Additionally, we can observe that if we escape the / \(backslash\) we may receive the output without the remainder again. 

![we may use double slash &apos;//&apos; and receive the truncated remainder output](../../../../.gitbook/assets/image%20%2851%29.png)

Why would we want to do this? Convenience, sometimes you would want to get one output or the other

To provide our Python 2 scripts with some forward compatibility, we may use the following line in our scripts:

_`from __future__ import absolute_import, division, print_function`_``

![](../../../../.gitbook/assets/image%20%2856%29.png)

## Input Function

If I wanted to get input from an user, assigning it to variable X:

We may prompt the user to type something:

![we would get a name error saying that &quot;hello&quot; is not defined](../../../../.gitbook/assets/image%20%2858%29.png)

The error is letting us know that that python does not have any objects named "hello"

If now, in contrast we do create an object called hello and assign it the value 242

![The value we initialized \(242\) and assigned to hello is now &quot;x&quot;](../../../../.gitbook/assets/image%20%2850%29.png)

This time we get no error because hello has been previously defined

It would not be uncommon to think that x = hello right?

![](../../../../.gitbook/assets/image%20%2849%29.png)

No. Why? Because it assigned to X the value of the hello object we had previously created

As you can imagine this behavior is not useful.

## raw\_input function

The raw\_input function helps us in this case. Fixes the issue because using raw input, when I type something

and I check the value of x, it is being assigned to what I typed. 

![This is typically what you want.](../../../../.gitbook/assets/image%20%2846%29.png)

**In Python 3:**

![The behavior raw\_input would have in Python 2 is default in Python 3](../../../../.gitbook/assets/image%20%2852%29.png)

In Python 3: the functions of raw\_input are performed by input. raw\_input does not exist in Python 3.

![raw\_input does not exist in Python 3.](../../../../.gitbook/assets/image%20%2853%29.png)

## How to run a script that works consistently on both versions

We may leverage the fact that raw\_input creates an error in python 3 and we can tell it to try raw input and catch the exception and NameError, use input function instead.

![Attempt to use raw\_input, otherwise, in case of NameError use input\(\)](../../../../.gitbook/assets/image%20%2847%29.png)

#### The following snippet was tested on Python 2.7 and Python 3.8 and demonstrate this concept:

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

[Full Source video](https://www.youtube.com/watch?v=h5AQeMhYTfU)

[Introduction Video to the full series](https://www.youtube.com/watch?time_continue=205&v=eiYemtNKS-M&feature=emb_logo) 

