# `/usr/local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the directory for housing all *Complete* stage' programs, applications,
libraries, default configuration files, documents, data files, etc.; faciliated
mainly for maintaining UNIX BSD filesystems inter-compatibilties. It is unused
by the MacOS system operations.

All files here are available to all users.

Generally, you **SHOULD ONLY** use this directory if you are a software
developer. Otherwise, to avoid confusion, this directory is hidden from the
end-user. Software developer can and know how to enable it.

This directory is **entirely optional** as it serves as a clean design
structure.




## The Localized UNIX System Resources (`usr/local`) Directory

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Since MacOS system operations are not using this directory, the following are
mainly for educational purposes and alignment for inter-compatibilties with
other UNIX-based OSes.

The `/usr/local` directory is one of the foundational directory for completing
the entire OS' functionalities. When `/usr/local` combines with the
[Common](/Common) FHS, you get a list of basic functional directories as such:

```
/usr/local/bin     - user supplied utilities programs and applications.
/usr/local/etc     - user supplied configuration files.
/usr/local/lib     - user supplied libraries used by user customized
                     non-critical programs and applications.
/usr/local/sbin    - user supplied non-critical system administration
                     programs and applications.
/usr/local/share   - user supplied architecture independent files.
/usr/local/src     - user supplied source files.
/usr/local/tmp     - user supplied content temporary workspaces.
```

The `/usr/local` directory also has other critical system directories that
provide various system roles:

```
/usr/local/include - user supplied include files (e.g. c header files).
```

Then, the OS can specify its specific directories such as:

```
FreeBSD
-------
/usr/local/libaARCH - user supplied cross CPU architectures library files.
/usr/local/libexec  - user supplied system daemons and system utilities executed
                      by other programs and applications.
/usr/local/www      - user supplied static web content by web servers (e.g.
                      Nginx).

Redhat Linux
------------
/usr/local/libexec  - user supplied system daemons and system utilities executed
                      by other programs and applications.
```

Feel free to explore all the sub-directories. When it's done. Head over
to [/home/USERNAME/.local](/UNIX/home/USERNAME/.local) for the user-only
filesystem layer.
