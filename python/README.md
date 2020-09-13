# Python

## Notes

These notes are based on Real Python's "[Getting the Most Out of a Python Traceback](https://realpython.com/courses/python-traceback/)" course:

- Traceback: A kind of report composed of function calls at a given point.
- In Python, it is recommended to read the traceback from the bottom up.
- There are differences in the output between the command line and the REPL environment (instead of filenames, `"<stdin>"` is obtained, for example).
- The `NameError` exception is useful for finding misspelled variables/parameters.
- The `SyntaxError` exception is raised during code parsing, that is, before execution.
- The `ValueError` exception is useful for detecting unpacking errors.
- Python has a [`traceback`](https://docs.python.org/3/library/traceback.html) module.

These notes are based on Jeff Knupp's "[Python with Context Managers](https://jeffknupp.com/blog/2016/03/07/python-with-context-managers/)" blog post:

- Context managers are used to managing resources properly. Working with files is a good example because opening a file consumes a file descriptor (a resource that is limited by the OS).
- `infile`: Abbreviation for _input file_.
- The Python interpreter opens about 5 files on startup.
- The `with` statement begins a kind of function in terms of scope.
- In general, all objects that have to be `close`d after being used are or should be context managers (like `pathlib.Path` objects, for example).
- Python has a [`contextlib`](https://docs.python.org/3/library/contextlib.html) module.
- The `contextlib.ContextDecorator` class allows you to create class-based context managers that can be used as decorators as well.

These notes are based on Ethan Smith's "[PEP 561 -- Distributing and Packaging Type Information](https://www.python.org/dev/peps/pep-0561/)" page:

- Stubs: These are files that contain only information about the types (no runtime code) and the filename ends in `.pyi`.
- A module can also be a file that contains stubbed type information.
- To include type information in a package, you need to do the following:
  - Add a marker file named `py.typed`.
    - This file applies recursively, that is, if a top-level package includes it, all its subpackages must support type checking as well.
    - For namespace packages, this file should be added to the submodules.
  - For the `py.typed` file to be installed with the package, add it to the `package_data` keyword argument of the `setup()` function: `package_data = {"foopkg": ["py.typed"]}`.
  - To include stub files, add `*.pyi` stubs next to the corresponding `*.py` files.
- It is also possible to create stub-only packages to be distributed separately. This requires the following:
  - The name of the stub-only package must be in the following format: _PACKAGENAME-stubs_ (for example, _foopkg-stub_ for the _foopkg_ package).

## Commands

- `python <script>.py 2> <log>.log`: `2>` is used here to redirect the standard error stream to a file.
- Check the maximum number of open file descriptors (on the command line): `ulimit -n`

## Snippets

**Log a traceback** (this snippet is based on Real Python's "[Getting the Most Out of a Python Traceback](https://realpython.com/courses/python-traceback/)" course):

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

**Class-based context manager** (this snippet is based on Jeff Knupp's "[Python with Context Managers](https://jeffknupp.com/blog/2016/03/07/python-with-context-managers/)" blog post):

```python
from typing import IO, Any


class File:
    def __init__(self, filename: str, mode: str) -> None:
        self.filename = filename
        self.mode = mode

    def __enter__(self) -> IO[str]:
        """
        It returns the resource to be managed.
        """

        self.file = open(self.filename, self.mode)
        return self.file

    def __exit__(self, *args: Any) -> None:
        """
        It is responsible for the (final) cleaning work and returns nothing.
        """

        self.file.close()
```

**Decorated context manager** (this snippet is based on Jeff Knupp's "[Python with Context Managers](https://jeffknupp.com/blog/2016/03/07/python-with-context-managers/)" blog post):

```python
from contextlib import contextmanager
from typing import Generator


@contextmanager
def open_file(path: str, mode: str) -> Generator:
    file = open(path, mode)  # Before `yield`: `__enter__()`
    yield file
    file.close()  # After `yield`: `__exit__()`
```
