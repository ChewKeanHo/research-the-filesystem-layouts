# `/var/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's temporary files and directories
workspaces.

Unlike `/tmp` directory, this directory **GET PERSISTED (without deletion on
reboot)** enabling post-booting forensic analytics use. It is always recommended
to clean up the temporary files after use to avoid any after-use corruption and
hogging unwanted storage spaces.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users and is restricted based on UNIX
filesystem permissions.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/tmp/
  trademark/
    product/
    ...

OR

/var/tmp/
  product/
    ...
```
