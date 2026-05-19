#  Linux Filesystem Hierarchy Standard

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a specific Filesystem Hierarchy Standard (FHS) for Linux-based operating
system (OS). This directory is to consolidate all Linux based OSes datapoints
before performing data abstractions for the common points.

This leaves room for innovation across time while maintaining common abstracted
patterns as a standards. It is a win-win for both situations.

Keep in mind that for Linux-based OSes, there are 2 internal factions duking out
for leading the development and standarizations:

1. The SystemD Community
  * https://lwn.net/Articles/1041316/
  * https://www.freedesktop.org/software/systemd/man/latest/file-hierarchy.html
  * https://github.com/systemd/systemd/issues/38563#issuecomment-3242736658
2. The SysV Community
  * https://www.devuan.org/
  * https://voidlinux.org/

Each communities may introduce their own innovations which is one of the cause
of Linux-based OSes fragmentations. While this research tries to cover as many
of them as possible, it cannot cover all the edge cases.




# Understanding The 4 Stages of Functionalities Extensions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Linux-based OS generally go through 4 stages of functionalities extensions:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. This only uses tools from the Root (`/`) directory
   excluding any system directories mounting (e.g. `/usr`). The goal varies
   depending on the system's holistic design ranging from operating entirely
   in a resources limited environment (e.g. as OpenWRT router firmware),
   performing operating systems self-rescue, or extending its functionality
   to the next level.
2. **Full Catalogue** - focuses on extending the OS' functionalities upto its
   full potentials. This involves mounting the OS system directories (`/usr`).
   The goal here is to extend the OS' capabilities upto to the OS distributor's
   warranted functionalities with their supplied software packages.
3. **Complete** - focuses on extending the OS' functionalities further
   with user introduced system-wide functionalities. This involves mounting
   the OS' localized system directories (`/usr/local`). The goal here is to
   completely make the OS fully functional with localized functionalities
   (e.g. custom downloaded software packages setup by the user for all users).
   At this point, the OS' functionalities are marked as completed.
4. **Personalized** - focuses on extending the OS' functionalities with
   user-specific system directories (`/home/[USERNAME]/.local`). This stage can
   change from time-to-time across different users as it based on the
   user-only configurations.




## The Root

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The root directory is the very foundational and critical directory
represented by `/` in FreeBSD OS. When root combines with [Common](/Common)
filesystem hierarchy, you get a list of basic functional directories such as:

```
/bin       - OS critical user utilities programs.
/etc       - OS critical configuration files and scripts.
/lib       - OS critical libraries used by `/bin` and `/sbin` programs.
/sbin      - OS critical system administration (sysadmins) programs.
/tmp       - OS temporary work files.
```

The root directory also has other system directories that provides
various system roles:

```
/boot      - OS critical bootloading component.
/efi       - OS critical EFI-type bootloading component (optional as some OS
             distributors mapped it as `/boot/efi` or `/boot/EFI` by default).
/dev       - OS mapped IO device nodes for hardware interactions.
/home      - OS users' home directories (optional).
/media     - OS mounted removable media like CDs, floppy disks, and portable
             disks.
/mnt       - temporary mountpoint for sysadmins and root users to troubleshoot
             mountable nodes and devices.
/proc      - OS process files (optional).
/root      - OS root account's home directory (optional).
/run       - OS critical runtime data component.
/srv       - OS general server payload data files which might be available very
             late at boot (optional).
/sys       - Linux kernel interactable user interface.
/usr       - OS UNIX Systems Resources for extended functionalities.
/var       - OS variable data directory like log, data, and spool files.
```




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to boot the OS critical component
up and running with minimum resources and be functionally operational.
This is known as `Emergency Mode` in many Linux OSes.

There are 2 possibilities:

* user use the operating system as it is (commonly seen in bare-metal
  embedded deployment like OpenWRT project); OR
* operating system expands to its full potentials by mount and load
  the `/usr` directory (common computing deployment).

You can explore each root layer's base directories in details. Once
done, head over to [`/usr`](/_Linux/usr) directory which is the second
layer for functionalities' expansions.
