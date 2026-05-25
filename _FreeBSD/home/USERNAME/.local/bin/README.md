# `/home/[USERNAME]/.local/bin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, programs and applications for extending the operating system
(OS)'s functionalities from *Complete* stage to *Personalized* stage. This means
that executables in this directory only appears specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure software without requiring
`root` or administrator(s) account for installation affecting the entire OS.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

Generally, you **SHOULD** place your files here.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
