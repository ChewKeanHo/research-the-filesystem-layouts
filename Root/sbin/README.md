# `/sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical system administrative programs
and applications of an operating system (OS) to function properly and minimally
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

In some `Linux`-based OSes like Oracle's Solaris (first to transform back in
2012) and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is
always being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, this directory is being symbolic linked to
`/usr/sbin` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/sbin` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/sbin` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD ONLY** place programs and applications that are very
critical in the early booting stage here without conflicting with existing POSIX
compliant programs. In the case of `/sbin` being symbolically linked to
`/usr/sbin`, you **MUST** place the content in `/usr/sbin` instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

All POSIX compliant registered programs based on IEEE POSIX1.0 list
(refer: https://pubs.opengroup.org/onlinepubs/9799919799/idx/utilities.html).

Among the known ones are:

```
shutdown - program to shutdown the operating system.
```

Optional programs (for robust functionalities) are:

```
fastboot - program to reboot the OS without checking the disk.
fasthalt - program to stop the OS without checking the disk.
fdisk    - program to configure partition table.
fsck     - program to check and repair a disk and partition.
fsck.*   - program(s) to check and repair specific disk and partition.
getty    - program to perform terminal robust configurations.
halt     - program to stop the OS.
ifconfig - program to configure a network interface.
init     - program to initialize the OS.
mkfs     - program to make filesystem format to a partition.
mkfs.*   - program to make specific filesystem format to a partition.
mkswap   - program to setup a swap area.
reboot   - program to reboot the OS.
route    - program to configure IP routing table.
swapon   - program to enable paging and swapping.
swapoff  - program to disable paging and swapping.
update   - program to flush filesystem periodically (daemon).
```
