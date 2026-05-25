# `/usr`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s distributor supplied
non-critical programs, applications, libraries, configurations, and files. It is
sharable but read-only for preventing unwanted temperment.

The goal is to expand the OS' functionalities from *Minimum & Critical* stage to
*Full Catalogue* stage.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## The UNIX System Resources (`usr`) Directory

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The `/usr` directory is one of the very foundational directory for extending the
base UNIX OS' functionalities. When `/usr` combines with the [Common](/Common)
filesystems, you get a list of basic functional directories as such:

```
/usr/bin           - OS distributor's supplied utilities programs and
                     applications.
/usr/include       - OS distributor's supplied include files (e.g. c header
                     files).
/usr/lib           - OS distributor's supplied libraries used by non-critical
                     programs and applications.
/usr/lib[ARCH]     - OS distributor's cross CPU architectures library files.
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
/usr/sbin          - OS distributor's supplied non-critical system
                     administration programs and applications.
/usr/share         - OS distributor's supplied architecture independent files.
/usr/src           - OS distributor's supplied source files.
```

* `/usr/etc` is unavailable as `/etc` is being used instead.
* `/usr/tmp` is unavailable as `/tmp` is being used instead.

The `/usr` directory also has other critical system directories that provides
various system roles:

```
/usr/freebsd-dist  - OS distributor's files.
/usr/libdata       - OS distributor's supplied miscellaneous utility data files.
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
/usr/ports         - The FreeBSD Ports Collection (optional).
/usr/tests         - The FreeBSD test suites.
```




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each `/usr` layer's base directories in details. Once done, head
over to [`/usr/local`](/_FreeBSD/usr/local) directory which is the last
system-level layer for functionalities expansions.
