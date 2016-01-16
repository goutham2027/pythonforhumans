---
title: Factorials of big numbers
---

#### Usage:
{% highlight python %}
import fact
fact.factorial(1000)
{% endhighlight %}

#### Code:
{% highlight python %}
import math

'''
Checks for factorial of n in factorials dictionary and
returns if it is, else it checks the difference between
 the highest number of factorial   in factorials dictionary
and n. If the difference is greater than the limit
 (default is 500) factorial is calculated for n in steps.
In python the default recursion depth is 1000.
'''

factorials = {0:1,1:1}

def factorial(n,limit=500):
    if factorials.has_key(n):
        return factorials[n]
    lastkey = sorted(factorials.keys())[-1]
    difference = n-lastkey
    if  difference < limit:
        return fact(n)
    else:
        incrementIndex =  int(math.ceil(difference/float(limit)))
        bigfactorial = 0
        for i in range(1,incrementIndex+1):
            currentN  =   lastkey + limit * i
            fact(currentN)
        return factorials[n]

''' Recursive function for  factorial '''
def fact(n):
    if factorials.has_key(n):
        return factorials[n]
    else:
        t = n * fact(n-1)
        factorials[n] = t
        return t

{% endhighlight %}
