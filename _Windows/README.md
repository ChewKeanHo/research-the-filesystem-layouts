# Microsoft Windows Filesystem Hierarchy Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is Microsoft Windows' common Filesystem Hierarchy Layout. Unlike any UNIX
system, Microsoft Windows relies on registry systems to locate key important
directories instead of structuring the directory in a specific pattern.

Therefore, the layout here are specifically analyzed based on a common drive
(e.g. `C:\`) single flat directory installation.




# Understanding The 4 Stages of Functionalities Extensions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Likewise, Microsoft Windows also generally go through 3 stages of
functionalities extensions:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. This only uses tools from the Root (`[DRIVE]\Windows`)
   directory excluding any system directories (e.g. `[DRIVE]\Program Files`).
   The goal varies depending on the system's holistic design ranging from
   operating entirely in a resources limited environment (e.g. before init
   stage), performing operating systems self-rescue, or extending its
   functionality to the next level.
2. **Complete** - focuses on extending the OS functionalities further with user
   introduced system-wide functionalities. This involves mounting the OS
   localized system directories (`[DRIVE]\Windows\Program Files`). The goal here
   is to completely make the OS fully functional with localized functionalities
   (e.g. custom downloaded software packages setup by the user for all users).
   At this point, the OS functionalities are marked as completed.
3. **Personalized** - focuses on extending the OS functionalities with
   user-specific system directories (`%LOCALAPPDATA%\Programs`). This stage can
   change from time-to-time across different users as it based on the
   user-only configurations.




## The Root

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The root directory is the very foundational and critical directory
represented by a Microsoft Windows' Drive assignment (e.g. `c:\`). It then uses
its own layout and common registries to locate and boot the Operating System up.

Microsoft Windows either boot into `Safe Mode` or `Full Mode`. Switching between
them involves a cold reboot.

Microsoft Windows also uses registry-based approach to locate a specific main
directory (e.g. `%WINDIR%` environment variable is always pointing to
`[DRIVE]\Windows`). They also use backslash (`\`) instead of forward slash (`/`)
to designate a directory separation in their pathing definitions.

For reducing learning curve, this layout maintains the use of backslash.




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to boot the OS critical component up and
running with minimum resources and be functionally operational.
