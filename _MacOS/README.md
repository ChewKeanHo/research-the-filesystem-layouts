# `MacOS` Standard Directories

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This section covers all Apple `MacOS` filesystem, a derived product from UNIX
BSD layer for Apple computers like MacBooks, Mac Mini, Mac Studios, etc.




# Understanding The 4 Stages of Functionalities Extensions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

`MacOS` generally go through 3 stages of functionalities extensions:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. This only uses tools from the Root System (`/System`)
   directory excluding any system directories mounting (e.g. `/Libraries` and
   `/Applications`). The goal varies depending on the system's holistic design
   ranging from operating entirely in a resources limited environment (e.g.
   before init stage), performing operating systems self-rescue, or extending
   its functionality to the next level.
2. **Complete** - focuses on extending the OS functionalities upto its full
   potentials. This involves mounting the OS system directories
   (`/Libraries` and `/Applications`). The goal here is to extend the OS
   capabilities upto to the OS distributor's warranted functionalities with
   their supplied software packages.
3. **Personalized** - focuses on extending the OS functionalities with
   user-specific system directories (`/home/[USERNAME]/Applications` and
   `/home/[USERNAME]/Libraries`). This stage can change from time-to-time across
   different users as it based on the user-only configurations.




## UNIX BSD Inter-Compatibility Filesystem

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

`MacOS` maintains its BSD inter-compatibility filesystem despite not using it at
all. The root directory is the very foundational and critical directory
represented by `/` in MacOS. When root combines with [Common](/Common)
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
