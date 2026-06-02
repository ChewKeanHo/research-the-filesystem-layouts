# `/usr/local`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, user supplied, programs,
applications, libraries files, configuration files, etc of an OS to function
properly. This means it can operate in `Multi-User` mode in BSD realm or
`Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Full Catalogue* stage to
*Complete* stage achieving full user-customized system-wide capabilities. All
payloads, filepaths, configurations, data, etc. are specific to this runtime
hardware and is completely customizable by system administrator (user with
`wheel` privilege).

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

Generally, you **SHOULD** place your system-wide files here for OS
customization. If you need the files to be accessible to a specific user,
use `${HOME}/[USERNAME]/.local` instead.




## Directory Structure

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When `/usr/local` combines with the [Common](/Common) filesystem, you get a list
of basic functional directories such as:

```
/usr/local/bin        - user supplied utilities programs and applications.
/usr/local/etc        - user supplied configuration files.
/usr/local/include    - user supplied include files (e.g. c header files).
/usr/local/lib        - user supplied libraries used by user customized
                        non-critical programs and applications.
/usr/local/lib[ARCH]  - user supplied cross CPU architectures library files.
/usr/local/libexec    - user supplied system daemons and system utilities
                        executed by other programs and applications.
/usr/local/sbin       - user supplied non-critical system administration
                        programs and applications.
/usr/local/share      - user supplied architecture independent files.
/usr/local/src        - user supplied source files.
/usr/local/tmp        - user supplied content temporary workspaces.
```

Then, the OS can specify its specific directories such as:

```
# FreeBSD
/usr/local/libdata    - user supplied misc. data files.
/usr/local/www        - user supplied static web content by web servers (e.g.
                        Nginx).
```
