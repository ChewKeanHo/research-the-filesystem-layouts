# `/root/.local/var`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific transient data files (e.g. state files, saved games files, web
server files, log files, etc) for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage. This means that
architecture independent data files in this directory only appears specifically
for this user.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

**Only `root` and administrators (users with `wheel` permission) can access the
directory**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, unless absolute necessary, you **SHOULD NOT** place anything here
**UNLESS** you are the OS distributor. This is to avoid any conflict with the
upstream's registries that will break the OS in any way. Use `/home/[USERNAME]`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/root/.local/var/
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

/root/.local/var/
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
