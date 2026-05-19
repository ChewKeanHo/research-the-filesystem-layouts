# `/Users/[USERNAME]/.local/libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied, non-critical,
user-specific, non-user (e.g. daemon server) programs and applications for
extending the operating system (OS)'s functionalities from *Complete* stage to
*Personalized* stage. This means that executables in this directory only appears
specifically for this user.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with the users'
customization. The secondary purpose is to facilitate a way to procure programs
and applications without using sysadmins or root account (e.g. `sudo`) that
affects the entire OS' security.

Generally, you **SHOULD** place your own custom programs and applications here.
It will be made available only for you.

All files here are available only to the owning user but full path calling is
required.

This directory **MUST NOT** have any sub-directory.

This directory is **ENTIRELY OPTIONAL** as it serves as a clean design
structure.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
