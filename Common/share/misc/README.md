# `share/misc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent miscellaneous system data
files. These files are accessible by various programs, applications, and
development project for an unified repository management.




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
