---
layout: post
title: Dive Into Python 3 学习笔记
categories: [编程语言, 笔记]
description: 深入python学习笔记
keywords: python, programming
---

### 1. First Python  Program

#### 1.1 Declaring Function

> **_When you need a function, just declare it. _**

```python
 def approximate_size(size, a_kilobyte_is_1024_bytes=True):

if __name__ == '__main__' :
    print(approximate_size(1000000, false))
```

#### 1.2 Writing Readable Code

```python
def approximate_size(size, a_kilobyte_is_1024_bytes=True):
	'''Convert a file size to human-readable form.
	Keyword arguments:
	size -- file size in bytes
	a_kilobyte_is_1024_bytes -- if True (default), use multiples of 1024
	if False, use multiples of 1000
	Returns: string

```

#### 1.3 The _import_ Search Path

	>>> import sys
	>>> sys
	<module 'sys' (built-in)>

#### 1.4 Everthing Is An Object
Everything in Python is an object. Strings are objects. Lists are objects. Functions are objects. Classes are objects. Class instances are objects. Even modules are objects.

>_**Everything is Python is object.**_

#### 1.5 Indenting Code
Python functions have no explicit begin or end , and no curly braces to mark where the function code starts and stops. The only delimiter is a **colon ( : )** and the indentation of the code itself.

#### 1.6 Exception
```python
	if size < 0:
		raise ValueError('number must be non-negative')

	try:
		import chardet
	except ImportError:
		chardet = None
```

#### 1.7 Unbound Variables
You never declare the variable multiple , _you just **assign** a value to it._ That’s OK, because Python lets you do that.

#### 1.8 Everthing is Case-senstive
All names in Python are case-sensitive: variable names, function names, class names, module names, exception names. If you can get it, set it, call it, construct it, import it, or raise it, it’s case-sensitive.

#### 1.9 Running Script
Well, modules are objects, and all modules have a built-in attribute *\__name__* . A module’s \__name__ depends on how you’re using the module. If you import the module, then \__name__ is the module’s filename, without a directory path or file extension.

	>>> import humansize
	>>> humansize.__name__
	'humansize'

### 2. Native Datatypes
1. **Booleans** are either True or False .
2. **Numbers** can be integers ( 1 and 2 ), floats ( 1.1 and 1.2 ), fractions ( 1/2 and 2/3 ), or even complex numbers.
3. **Strings** are sequences of Unicode characters, e.g. an HTML document.
4. **Bytes** and byte arrays, e.g. a JPEG image file.
5. **Lists** are ordered sequences of values.
6. **Tuples** are ordered, immutable sequences of values.
7. **Sets** are unordered bags of values.
8. **Dictionaries** are unordered bags of key-value pairs.

#### 2.1 Bolleans
> _**You can use virtually any expression in a bollean.**_

#### 2.2 Numbers
Python supports both **integers** and **floating** point numbers. There’s no type declaration to distinguish them; Python tells them apart by the presence or absence of a decimal point.

	>>> type(1)
	<class 'int'>
	>>> type(2.0)
	<class 'float'>
	>>> int(2.5)
	2

Python isn’t limited to integers and floating point numbers. It can also do all the fancy math you learned in high school and promptly forgot about.

	>>> import fractions 1
	>>> x = fractions.Fraction(1, 3) 
	>>> x
	Fraction(1, 3)
	>>> x * 2
	Fraction(2, 3)

>_**Zero values are false, and non-zero values are true.**_

#### 2.3 Lists

#### 2.4 Tuples

#### 2.5 Sets

#### 2.6 Dictionaries

#### 2.7 None

### 9. Uint Testing

>_**Every test is  a single island.**_

• ...run completely by itself, without any human input. Unit testing is about automation.
• ...determine by itself whether the function it is testing has passed or failed, without a human interpreting the results.
• ...run in isolation, separate from any other test cases (even if they test the same functions). Each test case is an island.

>_**Write a test that fails, then code until it passes.**_

#### test class
```python
import unittest
class KnownValues(unittest.TestCase):
	...
	def test_to_roman_known_values(self):
	...
if __name__ == '__main__':
	unittest.main()
```

>_**The pythonic way to halt and catch fire is to raise an exception.**_

```python
class ToRomanBadInput(unittest.TestCase):
    def test_too_large(self):
        '''to_roman should fail with large input'''
        self.assertRaises(roman2.OutOfRangeError, roman2.to_roman, 4000)
```

### 10. Refactoring
* Designing test cases that are specific, automated, and independent
* Writing test cases before the code they are testing
* Writing tests that test good input and check for proper results
* Writing tests that test bad input and check for proper failure responses
* Writing and updating test cases to reflect new requirements
* Refactoring mercilessly to improve performance, scalability, readability, maintainability, or whatever other -ility you’re lacking

### 11. File

>_**The default encoding is platform-dependent.**_

Take a look inside the RedirectStdoutTo class. This class is a custom context
manager. Any class can be a context manager by defining two special methods: **\__enter__() and \__exit__()** .

### 12. XML

### 13. Serializing Python Objects

### 14. HTTP Web Services
You should use **httplib2** , an open source third-party library that implements HTTP more fully than **http.client** but provides a better abstraction than **urllib.request** .
