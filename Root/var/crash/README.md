# `/var/crash`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) kernel and other crash dump
data report files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `crash(8)` and `savecore(8)` for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  trademark/
    product/
      file1.log
      file2.log
      ...

# OR

/var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  product/
    file1.log
    file2.log
    ...
```
