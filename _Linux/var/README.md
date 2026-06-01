# `/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for all operating system (OS)'s transient and
stateful data files (e.g. log files, saved files, databases, email files) to
function properly and minimally.

The goal is to provide flexibilities beyond configurations enabling the OS to
operate transiently across time even when the OS is operating in `Single-User`
mode in BSD realm or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, this directory is being symbolic linked to
`/usr/bin` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/bin` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/bin` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD ONLY** place data files used by programs and
applications supplied by the OS distributor here. Otherwise, you can use
`/usr/local/var` or `${HOME}/.local/var` layers instead.




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
