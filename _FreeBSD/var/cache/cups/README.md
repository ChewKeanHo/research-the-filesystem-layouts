# `/var/cache/cups`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s printing files from CUPS
service.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `cups(1)` for specifications.

The file extension can be anything.

It is a practice to house the files using `trademark` and `product` naming
pattern. This can significantly reduces the naming collision for common names.

Here are the examples:

```
/var/cache/cups/
  trademark-product.bin
  ...

OR

/var/cache/cups/
  trademark-product.bin
  ...
```
