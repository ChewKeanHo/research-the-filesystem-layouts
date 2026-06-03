# `/etc/pam.d`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s Pluggable Authentication
Modules (PAM) library files. This means it can operate in `Single-User` mode in
BSD realm or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

FreeBSD practices the use of `/usr/local/etc` so use `/usr/local/etc/pam.d`
instead. Therefore, generally, you **SHOULD NOT** place or modify the
configuration files that are very critical to the OS.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `pam(3)` and `pam.conf(5)` manuals for specifications, configuration,
precise naming pattern, and conventions before editing anything inside this
directory.

Generally, it is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/etc/pam.d/
  trademark-product-setting1
  trademark-product-setting2
  ...

OR

/etc/pam.d/
  product-setting1
  product-setting2
  ...
```
