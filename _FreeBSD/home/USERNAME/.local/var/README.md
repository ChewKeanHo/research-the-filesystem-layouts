# `/home/[USERNAME]/.local/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific transient data files (e.g. state files, saved games files, web
server files, log files, etc) for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage. This means that
architecture independent data files in this directory only appears specifically
for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure software without requiring
`root` or administrator(s) account for installation affecting the entire OS.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Generally, you **SHOULD** place your files here.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/home/[USERNAME]/.local/var/
  trademark/
    product/
      log/
        access.log
        info.log
        ...
      cache/
        icons/
          banner_1200x1200.svg
          ...
      ...

# OR

/home/[USERNAME]/.local/var/
  product/
    log/
      access.log
      info.log
      ...
    cache/
      icons/
        banner_1200x1200.svg
        ...
    ...
```
