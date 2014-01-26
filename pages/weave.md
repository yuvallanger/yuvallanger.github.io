---
title: _
---
# Accessing an array and its metadata through C/C++ in *scipy.weave.inline()*

* Accessing an array *foo* with *foo.ndim == 3*:
    - The array itself will be accessable through the *FOO3(i, j, k)* function.
    - Array assignments will be the same. *FOO3(i, j, k) = bar;*
    - *foo.shape* will be accessable through the *Nfoo[]* array.


## The inline code:

~~~ { .cpp }

long dim1, dim2, dim3;

dim1 = Nfoo[0]; // dimension access.
dim2 = Nfoo[1];
dim3 = Nfoo[2];

FOO3(0,0,0) = 1; // array assignment
return_val = FOO3(0,0,0); // array access.

~~~

## The Python code:

~~~ { .python }
import scipy
import scipy.weave
inline_code = r"""
put C/C++ code in here
"""
foo = scipy.arange(3**3).reshape((3,3,3))
scipy.weave.inline(inline_code, foo)
~~~

# Using Python functions in weave.inline

Call *foo.call(py:tuple arg)*.

# Links

* At Weave and Numpy array arguments: [Scipy's Weave page](http://www.scipy.org/Weave)
* [Calling Python functions from inline C with scipy.weave (stackoverflow)](http://stackoverflow.com/questions/5929600/calling-python-functions-from-inline-c-with-scipy-weave)
