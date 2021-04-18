# Getting the Most Out of a Python Traceback

> **Source**: Real Python's "[Getting the Most Out of a Python Traceback](https://realpython.com/courses/python-traceback/)" course.

- Traceback: A kind of report composed of function calls at a given point.
- In Python, it is recommended to read the traceback from the bottom up.
- There are differences in the output between the command line and the REPL environment (instead of filenames, `"<stdin>"` is obtained, for example).
- The `NameError` exception is useful for finding misspelled variables/parameters.
- The `SyntaxError` exception is raised during code parsing, that is, before execution.
- The `ValueError` exception is useful for detecting unpacking errors.
- Python has a [`traceback`](https://docs.python.org/3/library/traceback.html) module.

## Snippets

**Log a traceback**:

```python
import logging

logger = logging.getLogger(__name__)

try:
    ...
except Exception as e:
    logger.exception("Error")
    ...
else:
    ...  # Code to be executed if the try clause does not raise an exception
```
