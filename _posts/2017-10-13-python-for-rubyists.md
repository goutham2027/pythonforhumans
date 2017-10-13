---
title: Python For Rubyists
tags: python
---
* TOC
{:toc}

#### Introduction

If you are familiar with any one of the programming language this article will
help you to jump directly to Python code.

Though the article's title states it's for rubyists, actually it is for everyone who is
familiar with a programming language.

All the code examples are based on python3.

Python code blocks are indented.

#### Setting up environment
ruby tool python equivalent

`Gemfile` is `requirements.txt`

`gem install <gem>` is `pip install <package>`

`rvm` is `virtualenv`

`byebug`is `pdb` or `ipdb`


#### Hello World
{% highlight python %}
print("Hello world")
{% endhighlight %}

#### Variables
{% highlight python %}
number = 10
name = "David"
bool_t = True
bool_f = False
{% endhighlight %}

#### String-Variable interpolation
{% highlight python %}
name = "foo"
print("Hello, my name is", name)

print("Hello, my name is {} and my age is {}".format(name, 10))
print("Hello, my name is {0} and my age is {1}".format(name, 10))
print("Hello, my name is {name} and my age is {age}".format(name='goutham', age=10))

my_info = {'name': 'foo', 'age': 10}
print("Hello, my name is {name} and my age is {age}".format(**my_info))
{% endhighlight %}

#### Datastructures
Python has 2 types of data structures immutable and mutable.
Immutable can be changed.
Mutable once defined cannot be changed.

4 data structures

+ String (immutable)
+ List (mutable)
+ Dictionary (mutable)
+ Tuple (immutable)

##### String (immutable)
{% highlight python %}
name = "hello"
name[0] = "a" # will throw an error

len(name) # 5
name.upper() # HELLO
"HELLO".lower() # hello
{% endhighlight %}

##### List (mutable)
{% highlight python %}
nums = [1, 2, 3, 4]
nums[0] = 0
print(nums) # [0, 2, 3, 4]

len(nums) # 4
nums.append(5)
print(nums) # [0, 2, 3, 4, 5]
len(nums) # 5

nums.append(2)
print(nums) # [0, 2, 3, 4, 5, 2]
nums.remove(2) # will remove the first occurrence of 2
print(nums) # [0, 3, 4, 5, 2]

nums.pop() # will remove the last element
print(nums) # [0, 3, 4, 5]
{% endhighlight %}

##### Dictionary (mutable)
{% highlight python %}
alphabets = {'a': 'apple', 'b': 'bat'}
print(alphabets) # {'a': 'apple', 'b': 'bat'}

len(alphabets) # 2
alphabets['c'] = 'cat'
print(alphabets) # {'a': 'apple', 'b': 'bat', 'c': 'cat'}

list(alphabets.keys()) # list of keys
list(alphabets.values()) # list of values
{% endhighlight %}

##### Tuple (immutable)
{% highlight python %}
names = ('Foo', 'Baz')
names[0] = 'Zoo' # throws an error

len(names) # 2
{% endhighlight %}

#### Conditionals
{% highlight python %}
fruit = "apple"

if fruit == "apple:
  print("fruit is apple")
elsif fruit == 'orange':
  print("fruit is banana")
else:
  print("fruit is neither an orange nor a banana"
{% endhighlight %}

{% highlight python %}
num = 6

if num % 2 == 0 and num % 3 == 0:
  print("{} is divisible by 6")
{% endhighlight %}

#### Loops
{% highlight python %}
i = 0
while i < 10:
  print(i)
  i += 1
{% endhighlight %}

{% highlight python %}
for i in range(10):
  print(i)

for i in [1,2,3]:
  print(i)

for i in "foo":
  print(i)
{% endhighlight %}

#### Functions
{% highlight python %}
def say_hello(names):
  for name in names:
    print("Hello, {}".format(name))

say_hello(['foo', 'baz'])


def say_hello(*names):
  for name in names:
    print("Hello, {}".format(name))

say_hello('foo', 'baz')
{% endhighlight %}

#### Slicing
http://pythoncentral.io/how-to-slice-listsarrays-and-tuples-in-python/


#### Classes
The classic example of object oriented programming.
{% highlight python %}
class Animal(object):
  # constructor
  def __init__(self, name, legs):
    self.name = name
    self.legs = legs

  def say_name(self):
    print("My name is {}".format(self.name))


class Dog(Animal):
  def __init__(self, name, legs):
    super(Dog, self).__init__(name, legs)

  def bark(self):
    print("Woof Woof!!!")

dog = Dog('dog', 4)
dog.say_name() # My name is Lucy
dog.bark() # Woof Woff!!!
{% endhighlight %}

##### Class methods
{% highlight python %}
class Animal(object):
  # constructor
  def __init__(self, name, legs):
    self.name = name
    self.legs = legs

  def say_name(self):
    print("My name is {}".format(self.name))

  @classmethod
  def with_2_legs(cls):
    print("Animals with 2 legs")
{% endhighlight %}

#### Misc
{% highlight python %}
# Finding the type of a variable
type(<variable_name>

# get object id
id(<var|object>
{% endhighlight %}
