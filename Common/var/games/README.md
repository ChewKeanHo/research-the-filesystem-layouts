# `var/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient game data files. These files are accessible by
various programs, applications, and development project for an unified
repository management.

Note that this directory houses the transient data files (e.g. saved games,
screenshots, etc). For resources files (e.g. game engine manifests,
configurations, models, etc), look for `share/games` directory instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/games/
  trademark/
    product/
      saves/
        title1.save
        title2.save
        ...
      settings.d/
        color.conf
        lang.conf
        ...
      custom/
        title1.map
        title2.map
        ...
      ...
    ...
  ...

OR

var/games/
  product/
    saves/
      title1.save
      title2.save
      ...
    settings.d/
      color.conf
      lang.conf
      ...
    custom/
      title1.map
      title2.map
      ...
    ...
  ...
```
