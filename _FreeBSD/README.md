#  Free Berkeley Software Distribution (FreeBSD) Filesystem Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is FreeBSD-specific Filesystem Layout for FreeBSD operating system (OS)
based on its Filesystem Hierarchy Standard (FHS).

> [!WARNING]
>
> This is not a rule. Depending on OS, the distrbutor designer can customize the
> layout on its own. To avoid constricting innovation, this layout is abstracted
> from existing UNIX-based OSes instead of enforcing them to all OSes.




## Primary Objective

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective is to produce a common mapping of the latest UNIX
filesystem evolution. This map allows an OS designer to decide and to maximize
inter-OS compatibility purposes for better portability and user experience.

You can explore each directory here in details.




## Understanding The 4 Stages of Powering Up

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, any OS (including Microsoft `Windows`) go through 4 stages:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. The goal varies but usually about OS self-rescue, boot
   selections, self-auditing, low-resources environment operations (e.g.
   embedded. This stage only uses the Root (`/`) directory layer.
2. **Full Catalogue** - focuses on extending the OS functionalities upto its
   distributor's designed full potentials. The goal is to extend the OS
   capabilities to the full functionalities warranted by the OS designer. This
   usually involves mounting `/usr` directory layer.
3. **Complete** - focuses on extending the OS functionalities further with
   user's localized system-wide capabilities. The goal here is to extend the
   OS capabilities further to cater user's system-wide customized
   functionalities. This usually involves mounting `/usr/local` directory layer.
4. **Personalized** - focuses on extending the OS functionalities specifically
   for a user. The goal here is to further customize the OS capabilities
   specifically for a user. This usually involves mounting `${HOME}/.local`
   directory layer. This stage can revert back to **Complete** stage from
   time-to-time whenever an user is logged in or out.

> [!NOTE]
>
> Most proprietary OSes notably Apple's `MacOS` and Microsoft `Windows` skip the
> **Full Catalogue** stage as they are not facing the open-source multiple
> distributors fragmentations like the open source OSes (e.g. `FreeBSD` and
> `Linux`-based OSes).




## The Root

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The root directory is the very fundational  and critical directory layer for
**Critical & Minimal** stage. When it combines with [Common](/Common)
filesystem layout, you get a list of basic functional directories such as:

```
/bin       - OS critical user utilities programs.
/etc       - OS critical configuration files and scripts.
/lib       - OS critical libraries used by `/bin` and `/sbin` programs.
/sbin      - OS critical system administration (sysadmins) programs.
/var       - OS variable data directory like log, data, and spool files.
```

> [!IMPORTANT]
>
> `/include`, `/share` and `/src` are too bloated at this stage. Therefore, they
> are always excluded.

The root directory also has other system directories that provide various system
roles. For examples (not exhaustive):

```
# FreeBSD
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
/proc        - OS legacy `procfs` interface (optional).
/rescue      - Statically linked programs for emergency recovery.
/root        - OS root account's home directory (optional).
/tmp         - OS temporary work files.
/usr         - OS UNIX Systems Resources for extended functionalities.


# Linux
/boot        - OS critical bootloading component.
/dev         - OS mapped IO device nodes for hardware interactions.
/efi         - OS critical UEFI bootloading component.
/home        - OS users' home directories (optional).
/lib[ARCH]   - OS critical multi-CPU architectures' inter-compatible library
               files.
/media       - OS mounted removable media like CDs, floppy disks, and portable
               disks.
/mnt         - temporary mountpoint for sysadmins and root users to troubleshoot
               mountable nodes and devices.
/proc        - OS legacy `procfs` interface.
/root        - OS root account's home directory (optional).
/run         - OS unified `tmpfs` interface.
/spool       - OS unified spooling `tmpfs` interface.
/srv         - OS unified service `tmpfs` interface.
/sys         - OS kernel interface.
/tmp         - OS temporary work files.
/usr         - OS UNIX Systems Resources for extended functionalities.


# MacOS
/dev         - OS mapped IO device nodes for hardware interactions.
/mnt         - temporary mountpoint for sysadmins and root users to troubleshoot
               mountable nodes and devices.
/root        - OS root account's home directory (optional).
/tmp         - OS temporary work files.
/usr         - OS UNIX Systems Resources for extended functionalities.
```
