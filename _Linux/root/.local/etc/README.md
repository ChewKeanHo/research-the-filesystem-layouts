# `/root/.local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, configuration files for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage. This means that
configurations in this directory only appears specifically for this user.

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

The use of `.d` configuration directory strategy also reduces the configuration
complexities and making maintainability easier by just updating 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
/root/.local/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/root/.local/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
