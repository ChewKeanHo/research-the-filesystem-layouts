# `/root/.local/var/crash`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses the `root` account's all crash dump data report files.

The goal is to expand the OS' functionalities from *Complete* stage to
*Personalized* stage achieving full per-user customization capabilities. All
payloads, filepaths, configurations, data, etc. are specific to this runtime
hardware and to the owning user.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are **ONLY** available to `root` account, and OS administrators
(users with `wheel` permission) for create, read, update, and delete operation.

In some `Linux`-based OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted user-oriented dedicated software like
flatpak package manager (e.g. `$ flatpak --user install`) for achieving rootless
operation.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

In Microsoft `Windows`, this directory is inter-compatible with other UNIX and
UNIX-like OSes for localized software package management.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `crash(8)` and `savecore(8)` for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/root/.local/var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  trademark/
    product/
      file1.log
      file2.log
      ...
    ...
  ...

# OR

/root/.local/var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  product/
    file1.log
    file2.log
    ...
  ...
```
