# `/Users/[USERNAME]/.local/var/cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user-specific, user supplied,
non-critical, volatile performance enhancing data files for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

This directory **MUST NOT** have any sub-directory.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you. You are **STRONGLY RECOMMENDED** to remove the files after
use for preventing data file poisoning.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The first sub-directory layer is a list of function oriented directories (e.g.
`log`, `mail`, `lock`, `cache`, `tmp`, `crash`, `www`, `spool`, ...). This is
defined by the OS' engineering specification.

Within each function oriented sub-directory, it is a practice to house the
configuration files using `trademark` and `product` sub-directories pattern.
This can significantly reduces the naming collision for common names.

Here are the examples:

```
/Users/[USERNAME]/.local/var/cache/
  trademark/
    product/
      icons/
        banner_1200x1200.svg
        ...
    ...
  ...

# OR

/Users/[USERNAME]/.local/var/cache/
  product/
    icons/
      banner_1200x1200.svg
        ...
  ...
```
