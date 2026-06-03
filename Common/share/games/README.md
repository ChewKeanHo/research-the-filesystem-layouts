# `share/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent game data files. These files
are accessible by various programs, applications, and development project for an
unified repository management.

Note that this directory houses the resources files (e.g. game engine manifests,
configurations, models, etc). For transient data files (e.g. saved games,
screenshots, etc), look for `var/games` directory instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/home/[USERNAME]/.local/share/games/
  trademark/
    product/
      dict.dat
      i18n.toml
      data.bin
      ...
    ...
  ...

OR

/home/[USERNAME]/.local/share/games/
  product/
    dict.dat
    i18n.toml
    data.bin
    ...
  ...
```
