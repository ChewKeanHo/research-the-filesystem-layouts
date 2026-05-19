# `/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) multi-purpose transient
variable data files like log files, data files, saved games files, databases,
states files, etc.

Some data files are sharable while some are not. Programs should check the
file's ownership and access permissions before performing any action.

All files here are available to all users.

Generally, you **SHOULD ONLY** place data files used by the programs
and applications here.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, *you want to avoid creating anything on the first sub-directory
layer and likely want to use `/var/lib` instead*. The first sub-directory layer
is a list of function oriented directories (e.g. `log`, `mail`, `lock`, `cache`,
`tmp`, `crash`, `www`, `spool`, ...). This is defined by the OS' engineering
specification.

Within each function oriented sub-directory, notably the commonly used
`/var/lib` data directory, it is a practice to house the configuration files
using `trademark` and `product` sub-directories pattern. This can significantly
reduces the naming collision for common names.

Here are the examples:

```
/var/
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

/var/
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
