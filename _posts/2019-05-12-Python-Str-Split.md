---
title: Python str split function
tags: python
---

Python str split function has a second argument maxsplit. If maxsplit is n, it splits it into n+1 parts.

{% highlight python %}
name = "firstname middlename last big biggername"

first, middle, last = name.split(" ", 2)
{% endhighlight %}

Output
{% highlight python %}
print(first) # firstname
print(middle) # middlename
print(last) # last big biggername
{% endhighlight %}
