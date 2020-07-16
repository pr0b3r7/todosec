# Python 2 vs Python 3 - WIP

[Full Source video](https://www.youtube.com/watch?v=h5AQeMhYTfU)

[Introduction Video to the full series](https://www.youtube.com/watch?time_continue=205&v=eiYemtNKS-M&feature=emb_logo) 

#### **In Python 2:** 

print is a statement

 

![](../../../.gitbook/assets/image%20%2833%29.png)

**In Python 3:** 

print is a function

![Functions need parenthesis around the arguments we&apos;re passing them](../../../.gitbook/assets/image%20%2831%29.png)

**In Python 2:** 

If we were to wrap our string in parenthesis

![It would also print without issues... But..](../../../.gitbook/assets/image%20%2834%29.png)

#### Why?

Because 'hello' in **Python 2** would be a tuple of a single object.

### What is a tuple?

Collection or two \(2\) or more objects. Tuples are represented by using parenthesis around the objects that comprise them.

**In Python 2:** 

Python 2 will just convert this back to a string



![It converts it to a string because it is a single object tuple](../../../.gitbook/assets/image%20%2836%29.png)

If we were to add a second object, it would be kept as a tuple after hitting enter



![In contrast with screenshot above, this time the tuple was not transformed to a string](../../../.gitbook/assets/image%20%2841%29.png)

This is not the behavior that would be observed in **Python 3**

![](../../../.gitbook/assets/image%20%2840%29.png)



Since print is a function in Python 3, the arguments would be passed to print \#\# function and they would be printed as expected



&gt;&gt;&gt; print\("hello", "goodbye"\)

&gt;&gt;&gt; hello goodbye



If we want our scripts to run in Python 2 and 3, we would want common operations such as print to run \#\#\# in both versions. How do we achieve this?



\# Importing futures



A solution to the problem stated above is given by the use of futures. "futures" make Python 2.6 &gt; behave like Python 3 for certain functions. In this case \*\*print\*\*



from \_\_future\_\_ import print\_function



If the module above is imported in Python 2, the print function - 



&gt;&gt;&gt; print\("hello", "goodbye"\)



- would behave the same way as in Python 3



&gt;&gt;&gt; hello goodbye



Now if after importing print\_function from \_\_future\_\_ we attempted to use the print function, it will never behave like a statement again \(native Python 2 behavior\)



&gt;&gt;&gt; print"hello"

   File "&lt;stdin&gt;", line 1

     print "hello"

                ^

SyntaxError: invalid syntax



In Python 3, if we were to \*\*from \_\_future\_\_ import print\_function\*\* it would just ignore it. 



\# Division



In Python 2, Floor Divison: Drops the remainder and returns only a whole number.



&gt;&gt;&gt; 3/2

1

&gt;&gt;&gt;



Python thinks: You're dividing an integer by an integer, you probably want and integer back

and drops the remainder. :\) 



If instead, we were to provide one of the numbers as a float, the returned result would be a float too.



&gt;&gt;&gt; 3/2.0

1.5

&gt;&gt;&gt;

&gt;&gt;&gt;



\#\#\#\# A floating point number aka "float", is a number that includes decimal portion.



Again, if we wanted to have Python 2 behave like Python 3, we may import \_\_future\_\_.



&gt;&gt;&gt;

&gt;&gt;&gt; from \_\_future\_\_ import division

&gt;&gt;&gt;

&gt;&gt;&gt; 3/2

1.5

&gt;&gt;&gt;



Why would we want to do this? Convenience, sometimes you would want to get one output or the other

we may use double slash "//"



&gt;&gt;&gt;

&gt;&gt;&gt; 3//2

1

&gt;&gt;&gt;



We would get a truncated result that drops the decimal point. 



To provide our Python 2 scripts with some forward compatibility, we may use the following line in our scripts:



from \_\_future\_\_ import absolute\_import, division, print\_function



\# Input Function



If I wanted to get input from an user, assigning it to variable X:

I can prompt the user to type something:

&gt;&gt;&gt; x = input\('type something: '\)

type something: hello

Traceback \(most recent call last\):

    File "&lt;stdin&gt;", line 1, in &lt;module&gt;

    File "&lt;string&gt;", line 1, in &lt;module&gt;

NameError: name "hello" is not defined



And we would get a name error saying that "hello" is not defined, saying that python does not have any object 

named hello



If now, in contrast we do create an object called hello and assign it the value 55

When we type hello after being prompted to type something:

&gt;&gt;&gt;

&gt;&gt;&gt; hello = 55

&gt;&gt;&gt;

&gt;&gt;&gt; x = input\("type something: \)

type something: hello

&gt;&gt;&gt;

&gt;&gt;&gt;

This time we get no error because hello has been previously defined \(l.128\)

Now you would think that x = hello right?



&gt;

&gt;&gt;&gt; x

55



No. Why? Because it assigned to X the value of the hello object we had previously created

As you can imagine this is not useful.



The raw\_input function helps us in this case. Fixes the issue because using raw input, when I type something

and I check the value of x, it is being assigned to what I typed. 



&gt;

&gt;&gt;&gt; x = raw\_input\("type something: "\)

type something: hello

&gt;&gt;&gt; x

'hello'

&gt;&gt;&gt;



This is typically what you want.





\#\# \_\# Python 3\_



&gt;&gt;&gt; x = input\('type something: '\)

type something: hello

&gt;&gt;&gt; x

'hello'

&gt;

In fact, in Python 3, there is no longer a raw\_input function. It is made input do what raw\_input does. Basically what

raw\_input was supposed to do. 

&gt;&gt;&gt; x = raw\_input\('type something: '\)

Traceback \(most recent call last\):

  File "&lt;stdin&gt;", line 1, in &lt;module&gt;

NameError: name 'raw\_input' is not defined

&gt;&gt;&gt;



How to run a script that works consistently on both versions then?!?!



We may leverage the fact that raw\_input creates an error in python 3 and we can tell it to try raw input and catch

the exception and NameError, use input function instead.



&gt;&gt;&gt; try:

&gt;       x = raw\_input\('type something: '\)

&gt;   except NameError:

&gt;       x = input\('type something: '\)

&gt;

&gt;type something: hello 

&gt;&gt;&gt;x

&gt;"hello"

&gt;

&gt;

&gt;



The following snippet was tested on Python 2.7 and Python 3.8 and demonstrate this concept:



from \_\_future\_\_ import absolute\_import, division, print\_function

from pip.\_vendor.distlib.compat import raw\_input





def get\_input\(prompt=''\):

    try:

        line = raw\_input\(prompt\)

    except NameError:

        x = input\(prompt\)

    return line





x = get\_input\('Type : '\)



print\(x\)





Full Source video: https://www.youtube.com/watch?v=h5AQeMhYTfU

Full Video Series introduction: https://www.youtube.com/watch?time\_continue=205&v=eiYemtNKS-M&feature=emb\_logo

