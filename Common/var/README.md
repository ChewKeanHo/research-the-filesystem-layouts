# `var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient and stateful data files. These files are
accessible by various programs, applications, and development project for an
unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, the first sub-directory layer is a list of function oriented
directories (e.g. `log`, `mail`, `lock`, `cache`, `tmp`, `crash`, `www`,
`spool`, ...).

Within each function oriented sub-directory, notably the commonly used
`var/lib` data directory, it is a practice to house the configuration files
using `trademark` and `product` sub-directories pattern. This can significantly
reduces the naming collision for common names.

Here are the examples:

```
var/
  cache/
    trademark/
      product/
        icons/
          banner_1200x1200.svg
          ...
  lib/
    trademark/
      product/
        icons/
          banner_1200x1200.svg
          ...
  log/
    trademark/
      product/
        access.log
        info.log
        ...
  ...

# OR

var/
  cache/
    product/
      icons/
        banner_1200x1200.svg
        ...
  lib/
    product/
      icons/
        banner_1200x1200.svg
        ...
  log/
    product/
      access.log
      info.log
      ...
  ...
```
