# parse: Inverse of Format

> **Source**: calmcode's [parse](https://calmcode.io/parse/introduction.html) tutorial.

- [parse](https://github.com/r1chardj0n3s/parse) package.
- `[parse("https://github.com/{owner}/{repo}/", url).named for url in urls]`: Use the `.named` property to get a dictionary.
- `p = compile("https://github.com/{owner}/{repo}/")`: To create a parser and _reuse_ the template.
