# `/var/db/freebsd-update`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) FreeBSD package updates and
temporary files `freebsd-update` program. Due to its processing nature, one
**MUST** carefully work here to prevent any data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications.

All files here are available to all users.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `freebsd-update(8)` for manual specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/db/freebsd-update/
  trademark/
    product/
      node1
      node2
      file1.data
      file2.data
      ...

# OR

/var/db/freebsd-update/
  product/
    node1
    node2
    file1.data
    file2.data
    ...
```
