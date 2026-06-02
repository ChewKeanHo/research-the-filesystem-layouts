# `/etc/udev`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s device static change
daemon configuration files facilitating `udev` behaviors. It can operate
minimally without any mounting (e.g. `/usr` is not mounted or absent). This
means it can operate in `Single-User` mode in BSD realm or `Emergency Mode` in
Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

In `FreeBSD`, it practices the use of `/usr/local/etc` so use
`/usr/local/etc/devd` instead. Therefore, generally, you **SHOULD NOT** place or
modify the configuration files that are very critical to the OS.

In `Linux`-based OSes, this directory is named as `/etc/udev`.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `udev` and `udev.conf` manuals for specifications.

Generally, it is a practice to house the files using `trademark` and `product`
naming pattern. This can significantly reduces the naming collision for common
names.

Here are the examples:

```
/etc/udev/
  trademark-product-setting1.conf
  trademark-product-setting2.conf
  ...

OR

/etc/udev/
  product-setting1.conf
  product-setting2.conf
  ...
```
