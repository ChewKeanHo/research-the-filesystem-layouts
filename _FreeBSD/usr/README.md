# `/usr`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all operating system (OS)'s distributor
supplied only programs, applications, libraries files, configurations files,
etc to extend the OS capabilities to distributor-grade quality. This means it
can operate in `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Minimum & Critical* stage to
*Full Catalogue* stage achieving full distributor-grade warranted capabilities.

To protect the resources from any user's temperment, this directory is usally
mounted as `read-only`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Use `/usr/local` or `${HOME}/[USERNAME]/.local`
instead.




## The UNIX System Resources (`usr`) Directory

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When `/usr` combines with the [Common](/Common) filesystem, you get a list of
basic functional directories such as:

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
# FreeBSD
/usr/etc           - Unused. `/etc` is used instead.
/usr/freebsd-dist  - OS distributor's files.
/usr/libdata       - OS distributor's supplied miscellaneous utility data files.
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
/usr/ports         - The FreeBSD Ports Collection (optional).
/usr/tests         - The FreeBSD test suites.
/usr/tmp           - Unused. `/tmp` is used instead.


# Linux
/usr/etc           - Unused. `/etc` is used instead. Only Red Hat Linux use it.
/usr/kerberos      - Unused by many OS distributors. Red Hat Linux does use
                     this directory.
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
/usr/share/factory - Unused by many OS distributors. SystemD uses this for
                     default configurations and data files restoration (factory
                     reset).
/usr/tmp           - Unused. `/etc` is used instead. Only Red Hat Linux use it.
```
