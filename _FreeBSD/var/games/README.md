# `/var/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) BSD heritage games' status,
saved, configuration, score, etc data files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/games/
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

/var/games/
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
