# `/usr`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing all *Full Catalogue* stage' programs,
applications, libraries, default configuration files, documents, data files,
etc.; faciliated mainly for maintaining UNIX BSD filesystems
inter-compatibilties. It is unused by the MacOS system operations.

All files here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## The UNIX System Resources (`usr`) Directory

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Since MacOS system operations are not using this directory, the following are
mainly for educational purposes and alignment for inter-compatibilties with
other UNIX-based OSes.

The `/usr` directory is one of the very foundational directory for extending the
base UNIX OS' functionalities. When `/usr` combines with the [Common](/Common)
filesystems, you get a list of basic functional directories as such:

```
/usr/bin           - OS distributor's supplied utilities programs and
                     applications.
/usr/lib           - OS distributor's supplied libraries used by non-critical
                     programs and applications.
/usr/sbin          - OS distributor's supplied non-critical system
                     administration programs and applications.
/usr/share         - OS distributor's supplied architecture independent files.
/usr/src           - OS distributor's supplied source files.
```

* `/usr/etc` is generally unavailable as `/etc` is being used instead. However,
  in some UNIX-like OS like Red Hat Linux, it is available for scoping down
  distributor supplied configuration files.
* `/usr/tmp` is generally unavailable as `/tmp` is being used instead. However,
  in some UNIX-like OS like Red Hat Linux, it is available for replacing the
  `/tmp` directory.

The `/usr` directory also has other critical system directories that provides
various system roles:

```
/usr/include       - OS distributor's supplied include files (e.g. c header
                     files).
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
```

Then, the OSes can specify its specific directories such as:

```
FreeBSD
-------
/usr/freebsd-dist  - OS distributor's files.
/usr/libdata       - OS distributor's supplied miscellaneous utility data files.
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
/usr/ports         - The FreeBSD Ports Collection (optional).
/usr/tests         - The FreeBSD test suites.


Red Hat Linux
-------------
/usr/etc           - OS distributor's supplied configuration files.
/usr/kerberos      - OS distributor's Kerberos-related binaries and files.
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
/usr/tmp           - OS distributor's "/usr" temporary files directory.


SystemD
-------
/usr/share/factory - OS distributor's default configurations and data files for
                     factory reset.

UAPI Linux
----------
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
```
