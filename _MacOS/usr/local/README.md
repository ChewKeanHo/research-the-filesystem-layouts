# `/usr/local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) user supplied,
system-wide available custom programs, applications and files for extending its
functionalities from *Full Catalogue* stage to *Complete* stage. This means it
can operate in `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as designed by its distributor and customized by the
system administrators. The sole reason with the split between `/usr` and
`/usr/local` is to ensure any user **DOES NOT** interfere with your OS'
distributor installed packages (they are in `/` and `/usr` levels) allowing them
to update the OS seamlessly and smoothly across time. This is why every setup
here is specfically only for this machine.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD** place your custom system-wide files here. If you wish
do it ONLY for a single specific user, place it inside his/her
`/home/[USERNAME]/.local` directory instead.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## The Localized UNIX System Resources (`usr/local`) Directory

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Since MacOS system operations are not using this directory, the following are
mainly for educational purposes and alignment for inter-compatibilties with
other UNIX-based OSes.

The `/usr/local` directory is one of the foundational directory for completing
the entire OS' functionalities. When `/usr/local` combines with the
[Common](/Common) FHS, you get a list of basic functional directories as such:

```
/usr/local/bin       - user supplied utilities programs and applications.
/usr/local/etc       - user supplied configuration files.
/usr/local/include   - user supplied include files (e.g. c header files).
/usr/local/lib       - user supplied libraries used by user customized
                       non-critical programs and applications.
/usr/local/lib[ARCH] - user supplied cross CPU architectures library files.
/usr/local/libexec   - user supplied system daemons and system utilities
                       executed by other programs and applications.
/usr/local/sbin      - user supplied non-critical system administration
                       programs and applications.
/usr/local/share     - user supplied architecture independent files.
/usr/local/src       - user supplied source files.
/usr/local/tmp       - user supplied content temporary workspaces.
```

Then, the OS can specify its specific directories such as:

```
FreeBSD
-------
/usr/local/libdata    - user supplied misc. data files.
/usr/local/www        - user supplied static web content by web servers (e.g.
                        Nginx).
```

Feel free to explore all the sub-directories. When it's done. Head over
to [/home/USERNAME/.local](/UNIX/home/USERNAME/.local) for the user-only
filesystem layer.
