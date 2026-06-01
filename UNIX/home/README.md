# `/home`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user level data directory. The first-level
sub-directory name is usually mapped to an user's username or user identity. The
control is defined by `/etc/passwd` therefore it is not a compulsory rule for
the strict username matching.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS'
implementations and usage especially on an user-less system.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The first layer is mapped against an user's username or user identity defined in
`/etc/passwd` by the OS' user management system. Anything within the user
directory is at the owner's own discretions.

```
/home/
  [USERNAME]/
    ...
```

Note that while technically one can create a user directory using sysadmins or
root accounts, one still need to update the OS' user management system for
home directory matching association (e.g. update `/etc/passwd`).

Therefore, when in doubt, always use `$ adduser` proper command instead.
