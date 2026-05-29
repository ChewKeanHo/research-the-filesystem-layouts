# `/home/[USERNAME]/.local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, configuration files for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage. This means that
configurations in this directory only appears specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure software without requiring
`root` or administrator(s) account for installation affecting the entire OS.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

Generally, you **SHOULD** place your files here.




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
/home/[USERNAME]/.local/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/home/[USERNAME]/.local/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
