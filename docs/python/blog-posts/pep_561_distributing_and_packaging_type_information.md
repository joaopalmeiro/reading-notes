# PEP 561 -- Distributing and Packaging Type Information

> **Source**: Ethan Smith's "[PEP 561 -- Distributing and Packaging Type Information](https://www.python.org/dev/peps/pep-0561/)" page.

- Stubs: These are files that contain only information about the types (no runtime code) and the filename ends in `.pyi`.
- A module can also be a file that contains stubbed type information.
- Include type information in a package:
  - Add a marker file named `py.typed`.
    - This file applies recursively, that is, if a top-level package includes it, all its subpackages must support type checking as well.
    - For namespace packages, this file should be added to the submodules.
  - For the `py.typed` file to be installed with the package, add it to the `package_data` keyword argument of the `setup()` function: `package_data = {"foopkg": ["py.typed"]}`.
  - To include stub files, add `*.pyi` stubs next to the corresponding `*.py` files.
- It is also possible to create stub-only packages (or partial stub-only packages) to be distributed separately:
  - The name of the stub-only package must be in the following format: `PACKAGE_NAME-stubs` (for example, `foopkg-stub` for the `foopkg` package).
  - It is not necessary to add the `py.typed` file as the name `PACKAGE_NAME-stubs` is sufficient.
  - Stub-only packages should indicate which version(s) of the runtime package are supported (through the `install_requires` keyword argument of the `setup()` function, for example).
  - Partial stub-only packages must include `partial\n` in a top-level `py.typed` file.
- A sample package with inline types is available [here](https://github.com/ethanhs/pep-561).
- A sample stub-only package is available [here](https://github.com/ethanhs/stub-package).
