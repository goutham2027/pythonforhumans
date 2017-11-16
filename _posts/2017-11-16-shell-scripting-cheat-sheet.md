---
title: Shell Scripting Cheat Sheet
tags: shell scripting
---
Linux shell scripting is cool but it's syntax is not (for me). I always have to search online
for syntax. This post will serve as a cheatsheet to shell scripting and
will always be WIP.


* TOC
{:toc}

#### Variables
{% highlight shell %}
name="Tom"
echo $name
{% endhighlight %}

#### Conditionals



#### Arrays
{% highlight shell %}
numbers=( 1 2 3 4 )
{% endhighlight %}

#### Loops
{% highlight shell %}
for num in ${numbers[@]}
do
  echo $num
done
{% endhighlight %}

#### Functions
{% highlight shell %}

say_hello()
{
  echo "Hello"
}

say_hello
{% endhighlight %}

