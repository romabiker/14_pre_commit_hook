# Quadratic Equations Solver

##Pre-commit

When running "git commit" git runs tests.py before commit. If tests.py fail the commit will be aborted.

##How to use

Move script into .git/hooks/
Make it runnable: $ chmod +x .git/hooks/pre-commit

##Code example
```
$ git commit -m'Test hook'
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/home/path/to/devman/14_pre_commit_hook/quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error

----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
.git/hooks/pre-commit: 5: [: 1: unexpected operator
```


# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
