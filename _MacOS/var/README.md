# `/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing all operating system's (OS) multi-purpose
transient variable data files like log files, data files, databases, etc;
faciliated mainly for maintaining UNIX BSD filesystems inter-compatibilties. It
is unused by the MacOS system operations.

Some data files are sharable while some are not. Do check the ownership and
access permissions before action.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Since MacOS does not use `/var` directory, one can more freedom to design the
sub-directories although it is highly recommended to comply with UNIX
conventions for highest inter-compatibilities between UNIX-based OSes.

Generally, *you want to avoid creating anything on the first sub-directory layer
and likely want to use `/var/lib` instead*. The first sub-directory layer is a
list of function oriented (e.g. `log`, `mail`, `lock`, `cache`, `tmp`, `crash`,
`www`, `spool`, ...) directories. This is defined by the OS' engineering
specification itself.

Within the function oriented sub directory, notably the commonly used `/var/lib`
data directory, it is a practice to house the configuration files using
`trademark` and `product` sub-directories organization. This can significantly
reduces the naming collision for common names.

Here are the examples with and without using `trademark` directory:

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
