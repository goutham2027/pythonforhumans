---
title: Binary to Text Script
---

{% highlight python %}
def changetobin(c):
    return [bin(ord(i)) for i in c]

def tostr(items):
    s = ''
    for item in items:
        item = item[2:]
        s = s+ chr(sum([(2**i)*int(item[(len(item))-i-1]) for i in range(0,len(item))]))
    return s

if __name__=="__main__":
    items = changetobin('python')
    print "output: "+ tostr(items)

{% endhighlight %}

