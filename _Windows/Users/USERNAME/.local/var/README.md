# `[DRIVE]/Users/[USERNAME]/.local/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing a single user's user-specific, user
supplied, non-critical transient and stateful data files of an operating
system (OS) to function properly. This means it can operate in `Multi-User` mode
in BSD realm or `Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Complete* stage to
*Personalized* stage achieving full per-user customization capabilities. All
payloads, filepaths, configurations, data, etc. are specific to this runtime
hardware and to the owning user.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to the owning user, `root` account, and OS
administrators (users with `wheel` permission) for create, read, update, and
delete operation.

In some `Linux`-based OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted user-oriented dedicated software like
flatpak package manager (e.g. `$ flatpak --user install`) for achieving rootless
operation.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

In Microsoft `Windows`, this directory is inter-compatible with other UNIX and
UNIX-like OSes for localized software package management.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




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
[DRIVE]/Users/[USERNAME]/.local/var/
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

[DRIVE]/Users/[USERNAME]/.local/var/
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
