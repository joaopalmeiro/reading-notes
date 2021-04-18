# Did you know it's possible to avoid bugs only by using types? Meet "Type Driven Development", a strong approach used to get rid of common bugs in the code and it can be used in Python

> **Source**: Carlos Villavicencio's "[Did you know it's possible to avoid bugs only by using types? Meet "Type Driven Development", a strong approach used to get rid of common bugs in the code and it can be used in Python](https://2020.pycon.co/ponencias/14/)" talk.

- Company: [Stack Builders](https://www.stackbuilders.com/).
- Type-Driven Development.
- _Duck_ typing emoji: 🦆.
- Static type checker for Python: [`mypy`](http://mypy-lang.org/).
- Emoji for _primitive_ types: 🦕 (sauropod).
- Carlos showed some examples of [type aliases](https://docs.python.org/3/library/typing.html#type-aliases).
- It is possible to use a literal ellipsis (`...`) if the call signature of a `Callable` is not yet known, for example.
- The annotations are stored in the `__annotations__` dictionary.
