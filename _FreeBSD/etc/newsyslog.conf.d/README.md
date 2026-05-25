# `/etc/newsyslog.conf.d`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s log rotation
configuration file using the `.d` configuration directory pattern where 1 file
is 1 configuration. This means it can operate in `Single-User` mode in BSD realm
or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

FreeBSD practices the use of `/usr/local/etc` so use
`/usr/local/etc/newsyslog.conf.d` instead. Therefore, generally, you
**SHOULD NOT** place or modify the configuration files that are very critical to
the OS.

Generally, you **SHOULD ONLY** place or modify the configuration files that are
very critical to the operating systems.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You **MUST** refer to `newsyslog(8)` manual for configuration, precise naming,
and conventions before editing anything inside this directory.

Generally, it is a practice to house the files using `trademark` and `product`
naming pattern. This can significantly reduces the naming collision for common
names.

Here are the examples:

```
/etc/newsyslog.conf.d/
  trademark-product-setting1.conf
  trademark-product-setting2.conf
  ...

OR

/etc/newsyslog.conf.d/
  product-setting1.conf
  product-setting2.conf
  ...
```
