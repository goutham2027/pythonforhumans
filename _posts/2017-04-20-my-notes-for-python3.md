---
title: My notes to Python3
categories: python3
tags: python3
---

#### Setting up python3
```
mkvirtualenv --python=python3.5 test_python3
python --version # Python 3.5.1
```

Note: The following is mostly from references.

* print is a function now. `print()`.

* `xrange` no longer exists and `range` behaves like `xrange`.

* `map`, `filter` returns iterators.

* `1/2` returns `0.5`. To get previous behavior use `1//2` which returns
  `0`.

* All text is unicode. And encoded unicode is binary data. `str` is for
  text and `bytes` is for data (binary). No `u` prefix for text, but `b`
  is required for binary data.



References:
https://docs.python.org/3.0/whatsnew/3.0.html
