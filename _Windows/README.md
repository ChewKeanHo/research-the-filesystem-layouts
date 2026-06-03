# Microsoft Windows Filesystem Hierarchy Layout

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is Microsoft Windows' common Filesystem Hierarchy Layout. Unlike any UNIX
system, Microsoft Windows relies on registry systems to locate key important
directories instead of structuring the directory in a specific pattern.

Therefore, the layout here are specifically analyzed based on a common drive
(e.g. `C:\`) single flat directory installation.




## Understanding The 4 Stages of Powering Up

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Generally, any OS (including Microsoft `Windows`) go through 4 stages:

1. **Critical & Minimal** - focuses on booting up the OS upto the minimal
   operational level. The goal varies but usually about OS self-rescue, boot
   selections, self-auditing, low-resources environment operations (e.g.
   embedded. This stage only uses the Root (`/`) directory called `Layer-1`.
2. **Full Catalogue** - focuses on extending the OS functionalities upto its
   distributor's designed full potentials. The goal is to extend the OS
   capabilities to the full functionalities warranted by the OS designer. This
   stage only uses `/usr` directory called `Layer-2`.
3. **Complete** - focuses on extending the OS functionalities further with
   user's localized system-wide capabilities. The goal here is to extend the
   OS capabilities further to cater user's system-wide customized
   functionalities. This stage only uses `/usr/local` directory called
   `Layer-3`.
4. **Personalized** - focuses on extending the OS functionalities specifically
   for a user. The goal here is to further customize the OS capabilities
   specifically for an user. This stage can revert back and forth with
   *Complete* stage whenever an user logged in or out of a session. This stage
   only uses `${HOME}/.local` directory called `Layer-4`.

> [!NOTE]
>
> Most proprietary OSes notably Apple's `MacOS` and Microsoft `Windows` skip the
> **Full Catalogue** stage as they are not facing the open-source multiple
> distributors fragmentations like the open source OSes (e.g. `FreeBSD` and
> `Linux`-based OSes).




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

This directory is accessible via the the following environment variables:

* `%SYSTEMDRIVE%` - NOTE: you need to append `\` manually.
