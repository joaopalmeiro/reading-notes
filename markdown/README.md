# Markdown

## Notes

Arctic Ice Studio and Sven Greb's [Markdown code style](https://arcticicestudio.github.io/styleguide-markdown/) ([repo](https://github.com/arcticicestudio/styleguide-markdown)):

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
- Headings:
  - Use [atx](http://www.aaronsw.com/2002/atx/intro)-style headings (`# H1`, for example) instead of [Setext](https://en.wikipedia.org/wiki/Setext) ones.
  - "Avoid using two or more headers with the same content in the same markdown file."
  - "Use an upper case letter as the first letter of a header, unless it is a word that always starts with lowercase letters (...). The other letters have the same case they would have in the middle of a sentence."
- "A horizontal rule must consist of three hyphens (`-`) without spaces."
- "Prefer absolute URLs instead of relative ones to improve the portability of the document."
- "Always use [reference links](https://github.github.com/gfm/#reference-link) instead of inline links except for inner anchor links (fragment identifiers)."
- "Use blocks for internal and external reference links separated by one empty line."
- Lists:
  - "Use continuous numerating marker for ordered list items [(`1. 2. 3. ...`)]."
  - "Use punctuation at the end of a list item when it contains a sentence that starts with an upper case letter or multiple sentences or paragraphs. Omit the punctuation for single words."
- "Use the HTML `<details>` tag to add collapsible content."
- "Prefer lists and only use tables for small, non-complex and single line content."
- "Always use spaces characters where two spaces are used for indentation."
- "(...) avoid using a character limit per line for flowing text, but try to use a maximum line length of 120 characters (including whitespaces) for all other document elements."
