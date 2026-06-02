# `/etc/skel`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all user home directory structure template.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is unused and is facilitated via its
`/System/Library/User Template` directory. Also the equivalent directory is part
of the `local domain`.

Generally, you **SHOULD ONLY** place or modify the template files and
directories here for new user creation.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `useradd` manual for specifications.
