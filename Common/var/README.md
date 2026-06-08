# `var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient, varying data and state files - hence the name
`var/`. It has well‑known functionally named first‑level sub-directories such as
but not limited to `var/db/` for databases and `var/log/` for traceable log
files.

These sub-directories are known to exist across all deployments. While not a
rule, using them improves compatibility and portability. If a functional
directory is missing (e.g., `var/messages`), one can define it after researching
other OS implementations. If any already defines such a directory, use that
definition when sensible.

On a read‑only hardware system, this directory is usually mounted on a small
read‑writable medium (e.g., EEPROM, flash memory). It is **ALWAYS** a best
practice to back up this directory.




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
