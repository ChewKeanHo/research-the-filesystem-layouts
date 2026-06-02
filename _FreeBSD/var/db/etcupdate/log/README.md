# `/var/db/etcupdate/log`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) temporary files and log for
`etcupdate` program. Due to its processing nature, one **MUST** carefully work
here to prevent any data poisoning or losses.

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

Refer `etcupdate(8)` manual for specifications.

The naming convention is **singular `log`** as it represent the entire logging
service.

The file extension can either be `.txt` or `.log`.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/db/etcupdate/log/
  trademark/
    product/
      20251201_info.log
      20251202_info.log
      ...

OR

/var/db/etcupdate/log/
  product/
    20251201_info.log
    20251202_info.log
    ...
```
