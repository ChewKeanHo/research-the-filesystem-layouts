# `.local/sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user-specific, user supplied,
non-critical, system adminstrative programs and applications for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

This directory **MUST NOT** have any sub-directory.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
