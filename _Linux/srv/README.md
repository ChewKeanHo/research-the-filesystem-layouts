# `/srv`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all site-specific data served by specific
Linux-based OSes like Red Hat Linux. This directory gives users the location of
data files for a particular service, such as FTP, WWW, or CVS.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

This directory is **ENTIRELY OPTIONAL** depending on the type of Linux-based
OSes. By default, it is absent. Only Ret Hat Linux is using this directory.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentation for the definitions.
