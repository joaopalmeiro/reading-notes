# Markdown

## Notes

Arctic Ice Studio and Sven Greb's [Markdown code style](https://arcticicestudio.github.io/styleguide-markdown/)

- Inline code spans (one backtick character) **should be** used to highlight:
  - Executables: `gcc`, `npm`, `go`, `python`.
  - Paths: `/etc/hosts`.
  - Version numbers: `0.2.0`.
  - Code (reserved keywords, builtins, and operators, for example): `this`, `true`/`false`, `String`, `=>`.
- Inline code spans **should not be** used for:
  - Project or proper names: React, GCC, Node.js, Rust.
  - Libraries: libgit2, libc, jackson-databind.
  - Packages and modules: react-dom, snowsaw, archlinux-keyring.
- "Don't use emphasis elements (bold or italics) to introduce a multi line named section. Use headers instead which is exactly the semantic meaning of headers. (...) Use a level 6 header if the meaning of the header section should not stand out great."
- Use [atx](http://www.aaronsw.com/2002/atx/intro)-style headings (`# H1`, for example) instead of [Setext](https://en.wikipedia.org/wiki/Setext) ones.
