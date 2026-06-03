# `sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses commandable system administrative programs and
applications for `root` account and system administrators (e.g. user with
`wheel` permission on UNIX-based operating system (OS)es) depending on its OS
layer's objective. Any executable be it a compiled application program artifact
or a shell script can be placed here.

This differs from other executable directories (e.g. `bin`) as they have the
tendency cause chaos to an OS (e.g. making it unbootable) in the hands of
inexperienced folks. Only system administrators and `root` account can access
them as commands.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The filename **MUST BE THE SAME** as desired command to call in terminal.
