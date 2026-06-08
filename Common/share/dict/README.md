# `share/dict`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses dictionary word‑list data files for programs to query,
ensuring accurate and validated output. These files must be CPU‑architecture
independent.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `FreeBSD` or `Linux`-based OSes' `look(1)` manual for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/dict/
  freebsd           # FreeBSD wording, jargons, etc.
  README
  propernames
  web2              # words from Webster's Second International
  web2a
  words
  trademark/
    product/
      hello.toml
      error.toml
      warning.toml
      info.toml
      ...
    ...
  ...
```
