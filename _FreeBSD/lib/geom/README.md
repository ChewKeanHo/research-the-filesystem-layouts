# `/lib/geom`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s GEOM library files. It
can operate minimally without any mounting (e.g. `/usr` is not mounted or
absent). This means it can operate in `Single-User` mode in BSD realm or
`Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD ONLY** place or modify the configuration files that are
very critical to the OS.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `geom` manual for specifications.

Generally, it is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/lib/geom/
  trademark-product-task1.so
  trademark-product-task2.so
  ...

OR

/lib/geom/
  product-task1.so
  product-task2.so
  ...
```
