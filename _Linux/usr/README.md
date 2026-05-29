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

The `/usr` directory also has other critical system directories that provides
various system roles:

```
/usr/etc           - Unavailable as `/etc` is being used by default. Red Hat
                     Linux does use this directory.
/usr/kerberos      - Unused by many OS distributors. Red Hat Linux does use
                     this directory.
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
/usr/share/factory - Unused by many OS distributors. SystemD uses this for
                     default configurations and data files restoration (factory
                     reset).
/usr/tmp           - Unavailable as `/tmp` is being used by default. Red Hat
                     Linux does use this directory.
```




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each `/usr` layer's base directories in details. Once done, head
over to [`/usr/local`](/_Linux/usr/local) directory which is the last
system-level layer for functionalities expansions.
