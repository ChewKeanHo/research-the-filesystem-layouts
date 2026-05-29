# `/var/log`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses production log files from one or many programs and
applications across the entire operating system (OS).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is marked **AS COMPULSORY TO EXIST** by Linux's Filesystems
Standards (https://specifications.freedesktop.org/fhs/latest/varRequirements.html).
However, in practice, this directory is **OPTIONAL** depending on the runtime
OS uses and specifications.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to rotate the log files before use (e.g. by datetime or
id number increment) to avoid post-use blaming or data loss.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `log`** as it represent the entire logging
service.

The file extension can either be `.txt` or `.log`.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/log/
  trademark/
    product/
      20251201_info.log
      20251202_info.log
      ...

OR

/var/log/
  product/
    20251201_info.log
    20251202_info.log
    ...
```
