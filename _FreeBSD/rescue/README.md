# `/rescue`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all the critical programs, applications,
configuration files, libraries, and data files for perfoming self-rescue to the
operating system (OS).

The goal is to have minimally sufficient programs enough for basic
functionalities for performing OS self-rescue. All programs and applications
here are available to root account users operating in `Single User` mode only.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD ONLY** place programs that are very critical at early
booting stage without conflicting with existing POSIX compliant programs.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to `rescue(8)` manual for specifications.
