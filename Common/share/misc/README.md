# `share/misc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses miscellaneous resource files. These files **MUST BE**
CPU‑architecture independent. While it can contain anything, such placement is
generally discouraged because every file's location should be identified before
distribution.

Any miscellaneous placement is a technical debt to be revisited. Ideally, this
directory is empty.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/misc/
  trademark/
    product/
      data.bin
      README.md
      restriction.toml
      ...
    ...
  ...

OR

share/misc/
  product/
    data.bin
    README.md
    restriction.toml
    ...
  ...
```
