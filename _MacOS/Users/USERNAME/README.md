# `/Users/[USERNAME]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a single user's all data directory.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

By default creation, this directory houses the following user directory with
slight deviation from the common UNIX [User](/User) pattern (notably `Videos` ->
`Movies` instead):

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

However, Apple recommend to hide them from any non-developer end-user for
preventing catastrophic human error. A developer should not have difficulty
locating them.
