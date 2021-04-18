# Python with Context Managers

> **Source**: Jeff Knupp's "[Python with Context Managers](https://github.com/jeffknupp/blog/blob/master/content/2016-03-07-python-with-context-managers.md)" blog post.

<!-- Previous URL: https://jeffknupp.com/blog/2016/03/07/python-with-context-managers/ -->

- Context managers are used to managing resources properly. Working with files is a good example because opening a file consumes a file descriptor (a resource that is limited by the OS).
- `infile`: Abbreviation for _input file_.
- The Python interpreter opens about 5 files on startup.
- The `with` statement begins a kind of function in terms of scope.
- In general, all objects that have to be `close`d after being used are or should be context managers (like `pathlib.Path` objects, for example).
- Python has a [`contextlib`](https://docs.python.org/3/library/contextlib.html) module.
- The `contextlib.ContextDecorator` class allows you to create class-based context managers that can be used as decorators as well.

## Snippets

**Class-based context manager**:

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

**Decorated context manager**:

```python
from contextlib import contextmanager
from typing import Generator


@contextmanager
def open_file(path: str, mode: str) -> Generator:
    file = open(path, mode)  # Before `yield`: `__enter__()`
    yield file
    file.close()  # After `yield`: `__exit__()`
```
