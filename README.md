# Python Debugging
Tools to debug in Python

1. Debugger

a) Python Debugger (PDB)

- With IPython Interpreter 

```python
import ipdb; ipdb.set_trace() 
```
or 
```python
from IPython import embed; embed();
```

- With Python interpreter

```python
import pdb; pdb.set_trace()
```
5 most used PDB commands are:

1. `l(ist)` - Displays 11 lines around the current line or continue the previous listing.
2. `s(tep)` - Execute the current line, stop at the first possible occasion.
3. `n(ext)` - Continue execution until the next line in the current function is reached or it returns.
4. `b(reak)` - Set a breakpoint (depending on the argument provided).
5. `r(eturn)` - Continue execution until the current function returns.

Other useful commands are:
1. `a(rgs)` - print argument list
2. `bt/ where` - stack trace, arrow indicates current frame
3. `c(ontinue)` - continue execution
4. `j(ump)` - jump line number
5. `p(rint)` - print value of expression
6. `p(retty)p(rint)` - pretty print value of expression
7. `q(uit)` - quit pdb
8. `d(own)` - move down the stack trace
9. `ret(urn)val(ue)` - return value of a function
10. `source` - get source code of an object
11. `u(p)` - move to upper stack trace


b) PUDB

2. Use print statement

```python
print()
```

3. USE UNIT TEST

a) PyTest

~~~
$ pip install -U pytest
~~~

For example, in __main.py__ , we have these functions:
```python
def add(a, b):
  return a + b
  
def multiply(a, b):
  return a * b
```

We can test them. Write these in __test_main.py__ .
```python
from main import add, multiply

def test_add(a, b):
  total = add(2, 3)
  assert total == 5
  
def test_multiply(a, b):
  product = multiply(2, 3)
  assert product == 6
```

Run the test
~~~
$ py.test
~~~

b) Use unittest module

__main__.py
```python
import unittest

def add(x, y):
    return x + y
 
# Examples of assert method
# assertEqual
# assertTrue
# assertFalse
class test_add(unittest.TestCase):
   def test(self):
       self.assertEqual(add(3,4), 7)
  
if __name__ == "__main__":
    unittest.main()
```

~~~
$ python main.py
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK
~~~


4. USE PUDB
