# `/root/.local/bin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, programs and applications for extending the operating system
(OS)'s functionalities from *Complete* stage to *Personalized* stage. This means
that executables in this directory only appears specifically for this user.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

**Only `root` and administrators (users with `wheel` permission) can access the
directory**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, unless absolute necessary, you **SHOULD NOT** place anything here
**UNLESS** you are the OS distributor. This is to avoid any conflict with the
upstream's registries that will break the OS in any way. Use `/home/[USERNAME]`
instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
