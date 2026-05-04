# `/Users`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user level data directory. The first-level
sub-directory name is mapped based on the user's username. The directory's
access are configured specifically to that user.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




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
