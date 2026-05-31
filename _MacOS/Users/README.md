# `/Users`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user level data directory. The first-level
sub-directory name is mapped based on the user's username. The directory's
access are configured specifically to that user. The control is defined by
Apple Account server with strict username matching.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The first layer is mapped against the username. Anything within the user
directory is at the owner's own discretions.

```
/Users/
  [USERNAME]/
    ...
```

Avoid creating user directory manually. Use MacOS' "Users & Accounts" settings
app to add or remove the user. Apple's user accounts are synchonized with the
Apple server.
