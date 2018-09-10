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
4. USE PUDB
