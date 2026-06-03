# `share/locale`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent localization data files.
These files are accessible by various programs, applications, and development
project for an unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD's `setlocale(3)` manual for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/locale/[LAND_ID]/
  trademark/
    product/
      encryption.mo
      sign.mo
      auth.mo
      ...
    ...
  ...

OR

share/locale/[LAND_ID]/
  product/
    encryption.mo
    sign.mo
    auth.mo
    ...
  ...
```
