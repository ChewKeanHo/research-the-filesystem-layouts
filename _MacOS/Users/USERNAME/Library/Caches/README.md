# `/Users/[USERNAME]/Library/Caches`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses re-creatable and performance-improving files specifically
for this user. The apps are generally responsible for their own caches files
including creating and removing them after use for avoiding data poisoning.

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding any breakage (e.g. signed signature). Let the installed apps handle
it.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `[APPNAME]`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/Users/[USERNAME]/Library/Caches/
  trademark/
    [APPNAME]/
      lib1.dat
      lib1_freebsd-amd64.dat
      kernel8.dat
      kernel8_freebsd-amd64.dat
      ...

# OR

/Users/[USERNAME]/Library/Caches/
  [APPNAME]/
    lib1.dat
    lib1_freebsd-amd64.dat
    kernel8.dat
    kernel8_freebsd-amd64.dat
    ...
```
