# `/sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system administrators (sysadmins) only
critical programs and applications of an operating system (OS) to function
properly and minimally without any mounting (e.g. `/usr` is not mounted or
absent). This means it can operate in `Single-User` mode.

The goal is to have minimally sufficient programs enough for basic
functionalities to perfrom critical tasks like mounting `/usr` UNIX System
Resources directory for functionalities extension, performing self-rescue, or
straight up operational in resources constraint environment such as but not
limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are **ONLY** available to sysadmins (users in `wheel` group) and
`root` account.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer seeing performance differences between
`/` and `/usr`, this directory is being symbolic linked to `/usr/sbin` instead;
unifying both directories. This reduces the separation complexities while
simplifying the package managements to target `/usr/sbin` only. **FreeBSD
however, have not seen to perform such implementation yet presumbly for backward
compatibility purposes.**

Generally, you **SHOULD ONLY** place programs that are very critical at early
booting stage without conflicting with existing POSIX compliant programs. In the
case of `/sbin` being symbolic linked to `/usr/sbin`, you **MUST NOT** place
anything here and use `/usr/sbin` exclusively instead.

This directory **MUST NOT** have any sub-directory.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

All programs here are registered programs that are usable across all UNIX and
UNIX-like OSes (POSIX Compliant). Among them are:

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
