# `/Users/[USERNAME]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a single user's all data directory.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory. The applies to all
directories here **except `Public`** which is available to all users.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here.

This directory is part of the `local domain`.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

By default, `MacOS` has the user-specific system applications as follows:

```
/Users/
  [USERNAME]/
    Applications/
    Library/
```

Then this directory houses the following user directory with slight deviation
from the common UNIX [User](/User) pattern (notably `Videos` -> `Movies`
instead):

```
/Users/
  [USERNAME]/
    Applications/
    Desktop/
    Documents/
    Downloads/
    Library/
    Movies/
    Music/
    Pictures/
    Public/
    Sites/
```

MacOS retains the traditional [Common](/Common) UNIX directories structure not
for end-user but for software developers. Upon combinations with the above,
the full structure becomes:

```
/Users/
  [USERNAME]/
    Applications/
    bin/                -> ${HOME}/.local/bin
    Desktop/
    Documents/
    Downloads/
    lib/                -> ${HOME}/.local/lib
    Library/
    Movies/
    Music/
    Pictures/
    Public/
    sbin/               -> ${HOME}/.local/sbin
    Sites/
    .local/
      bin/
      etc/
      include/
      lib/
      sbin/
      share/
      var/
```

However, Apple recommend to hide them from any non-developer end-user for
preventing catastrophic human error. A developer should not have difficulty
locating them.
