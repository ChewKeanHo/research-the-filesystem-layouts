# `/usr/share/factory/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) multi-purpose transient
variable data files like log files, data files, saved games files, databases,
states files, etc.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All files names and locations are registered by
OS distributor. Therefore, they are available consistently and uniformly across
all the machines.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Keep in mind that everything in this directory
resets the root filesystems to factory default settings.

This directory is a factory reset default configurations files that will
overwrite the `/var` directory when triggered.




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
/usr/share/factory/var/
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

/usr/share/factory/var/
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
