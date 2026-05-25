# `/etc/dma`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s `dma` Mail Transport
Agent (MTA) for email acceptance and delivery using  a locally-installed
Mail User Agents (MUA). This means it can operate in `Single-User` mode in
BSD realm or `Emergency Mode` in Linux realm.

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

Refer `dma` manual for specifications.

Generally, it is a practice to house the files using `trademark` and `product`
naming pattern. This can significantly reduces the naming collision for common
names.

Here are the examples:

```
/etc/dma/
  trademark-product-setting1.conf
  trademark-product-setting2.conf
  ...

OR

/etc/dma/
  product-setting1.conf
  product-setting2.conf
  ...
```
