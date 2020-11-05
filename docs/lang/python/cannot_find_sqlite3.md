# Cannot find _sqlite3 in Python

## Fix

Python was compiled without the optional extra libraries. You'll need to install the extra libraries, then force `pyenv` to recompile your Python version. If you're using this version in a virtualenv, you'll also need to remake any virtualenvs that use this version.

Take a look at [this page](https://github.com/pyenv/pyenv/wiki/common-build-problems) for the recommended list of prerequisites to install for Python to work correctly and install the appropriate options for your operating system. After that, you'll need to force `pyenv` to recompile the problematic version of Python:

```sh
# Here, we're assuming the issue is with python 3.9.0
pyenv install 3.9.0 --force
```

## Why does this happen?

Python, by default, only comes with enough functionality to run the language. A lot of extra modules (like .zip / .tar support, readline, zlib, openssl, and sqlite3 just to name a few) are not included in a base install. When Python is compiled, you'll need to have the extra libraries required to power these bits of functionality already installed on your computer; otherwise, they simply won't work (even if you install them after compilation!).
