#  Free Berkeley Software Distribution (FreeBSD) Filesystem Hierarchy Standard

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is FreeBSD-specific Filesystem Hierarchy Standard (FHS) for FreeBSD
operating system (OS).




# Understanding The 4 Stages of Functionalities Extensions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

FreeBSD OS generally go through 4 stages of functionalities extensions:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. This only uses tools from the Root (`/`) directory
   excluding any system directories mounting (e.g. `/usr`). The goal varies
   depending on the system's holistic design ranging from operating entirely
   in a resources limited environment (e.g. before init stage), performing
   operating systems self-rescue, or extending its functionality to the next
   level.
2. **Full Catalogue** - focuses on extending the OS functionalities upto its
   full potentials. This involves mounting the OS system directories (`/usr`).
   The goal here is to extend the OS capabilities upto to the OS distributor's
   warranted functionalities with their supplied software packages.
3. **Complete** - focuses on extending the OS functionalities further with user
   introduced system-wide functionalities. This involves mounting the OS
   localized system directories (`/usr/local`). The goal here is to completely
   make the OS fully functional with localized functionalities (e.g. custom
   downloaded software packages setup by the user for all users). At this point,
   the OS functionalities are marked as completed.
4. **Personalized** - focuses on extending the OS functionalities with
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

> [!NOTE]
>
> `/share` and `/src` are too much for this level (either bloat the entire
> pre-init OS or simply not used). Hence, they are excluded as always.

The root directory also has other system directories that provide various system
roles:

```
/boot        - OS critical bootloading component.
/compat      - Files supporting binary compatibilities with other operating
               systems like linux (`/compat/linux`).
/dev         - OS mapped IO device nodes for hardware interactions.
/entropy     - Provides initial state to random number generator (RNG).
/home        - OS users' home directories (optional).
/libexec     - OS critical system files not importable as libraries but not
               suitable for any users to call upon.
/media       - OS mounted removable media like CDs, floppy disks, and portable
               disks.
/mnt         - temporary mountpoint for sysadmins and root users to troubleshoot
               mountable nodes and devices.
/net         - Automounted Network Area Storage (NAS) share mounting.
/nonexistent - Home directory for users who do not need an actual '/home'
               directory (optional).
/rescue      - Statically linked programs for emergency recovery.
/root        - OS root account's home directory (optional).
/usr         - OS UNIX Systems Resources for extended functionalities.
/var         - OS variable data directory like log, data, and spool files.
```




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to boot the OS critical component up and
running with minimum resources and be functionally operational. This is known as
`Single User` operating mode.

There are 2 possibilities:

* user use the operating system as it is (commonly seen in bare-metal embedded
  deployment like OpenWRT project); OR
* operating system expands to its full potentials by mount and load the `/usr`
  directory (common computing deployment).

You can explore each root layer's base directories in details. Once done, head
over to [`/usr`](/_FreeBSD/usr) directory which is the next stage of OS
functionalities expansions.
