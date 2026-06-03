# `share/man`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent manual documentation data
files. These files are accessible by various programs, applications, and
development project for an unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD's `man(1)` manual for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/man/
  trademark/
    product/
      man1/
        amd64
        aarch64
        ...
      man2/
        amd64
        aarch64
        ...
      ...
    ...
  ...

OR

share/man/
  product/
    man1/
      amd64
      aarch64
      ...
    man2/
      amd64
      aarch64
      ...
    ...
  ...
```
