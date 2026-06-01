# `/libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical, non-callable programs and
applications of an operating system (OS) to function properly and minimally
without any mounting (e.g. `/usr` is not mounted or absent). This means it can
operate in `Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for OS capabilities extension, performing self-rescue, or
straight up being operational in this resources constraint environment such as
but not limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

All programs and applications here are **NOT AVAILABLE** as callable commands
for any users. Sysadmins (users in `wheel` group) and root account must execute
them via full filepath calling manually.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, this directory is being symbolic linked to
`/usr/libexec` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/libexec` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/libexec` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD ONLY** place programs and applications that are very
critical at early booting stage without conflicting with existing libraries. In
the case of `/libexec` being symbolic linked to `/usr/libexec`, you **MUST NOT**
place anything here and use `/usr/libexec` exclusively instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
