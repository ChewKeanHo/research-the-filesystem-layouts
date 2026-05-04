# `/Users/[USERNAME]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user level data directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

By default creation, this directory houses the following user directory with
slight deviation from the common UNIX [User](/User) pattern:

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

All directories **except `Public`** are inaccessible by other users on the
system by default.

MacOS retains the traditional [Common](/Common) UNIX directories structure not
for end-user but for software developers. Upon combinations with the above,
the full structure becomes:

```
/home/
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

However, Apple recommend to hide them from any end-user for human error
prevention. A software developer knows how to enable them.
