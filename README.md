[![License](https://img.shields.io/badge/license-%20BSD--3-blue.svg)](../master/LICENSE)


## Git bisect exercise

### Motivation

The motivation for this exercise is to be able to do archaeology with Git on a
source code where the bug is difficult to see visually. **Finding the offending
commit is often more than half the debugging**.


### Background

The script `get_pi.py` approximates pi using terms of the Nilakantha series. It
should produce 3.14 but it does not. The script broke at some point and
produces 3.57 using the last commit:

```
$ python get_pi.py

3.57
```

At some point within the 500 first commits, an error was introduced. The only
thing we know is that the first commit worked correctly.


### Your task

Clone or fork this repository and use `git bisect` to find the commit which
broke the computation.
