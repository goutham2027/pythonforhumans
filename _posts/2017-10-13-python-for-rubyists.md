---
title: Python For Rubyists
tags: python code
---
All the code examples are based on python3
Python code blocks are indented.

#### Hello World
```
print("Hello world")
```

#### variables
```
number = 10
name = "David"
```

#### Datastructures
Python has 2 types of data structures immutable and mutable.
Immutable can be changed.
Mutable once defined cannot be changed.

4 data structures
* String (immutable)
* List (mutable)
* Dictionary (mutable)
* Tuple (immutable)

#### String (immutable)
```
name = "hello"
name[0] = "a" # will throw an error

len(name) # 5
name.upper() # HELLO
"HELLO".lower() # hello
```

#### List (mutable)
```
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
```

#### Dictionary (mutable)
```
alphabets = {'a': 'apple', 'b': 'bat'}
print(alphabets) # {'a': 'apple', 'b': 'bat'}

len(alphabets) # 2
alphabets['c'] = 'cat'
print(alphabets) # {'a': 'apple', 'b': 'bat', 'c': 'cat'}

list(alphabets.keys()) # list of keys
list(alphabets.values()) # list of values
```

#### Tuple (immutable)
```
names = ('Foo', 'Baz')
names[0] = 'Zoo' # throws an error

len(names)
```

#### conditionals
```
fruit = "apple"

if fruit == "apple:
  print("fruit is apple")
elsif fruit == 'orange':
  print("fruit is banana")
else:
  print("fruit is neither an orange nor a banana"
```

```
num = 6

if num % 2 == 0 and num % 3 == 0:
  print("{} is divisible by 6")
```

#### Loops
```
i = 0
while i < 10:
  print(i)
  i += 1
```

```
for i in range(10):
  print(i)

for i in [1,2,3]:
  print(i)

for i in "foo":
  print(i)
```

#### Functions
```
def say_hello(names):
  for name in names:
    print("Hello, {}".format(name))

say_hello(['foo', 'baz'])


def say_hello(*names):
  for name in names:
    print("Hello, {}".format(name))

say_hello('foo', 'baz')
```

#### Slicing
http://pythoncentral.io/how-to-slice-listsarrays-and-tuples-in-python/

#### Variable interpolation
