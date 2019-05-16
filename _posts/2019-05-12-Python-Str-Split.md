---
title: Resources
tags: resource
---

Python str split function has a second argument maxsplit. If maxsplit is n, it splits it into n+1 parts.

```python
name = "firstname middlename last big biggername"

first, middle, last = name.split(" ", 2)
```

Output
```python
print(first) # firstname
print(middle) # middlename
print(last) # last big biggername
