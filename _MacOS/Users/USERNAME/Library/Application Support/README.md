# `/Users/[USERNAME]/Library/Application Support`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses app data except those associated with user's documents for
this specific user. Files like app-created data files, configuration files,
templates, or other fixed or modifiable resources managed by an app.

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.

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
/Users/[USERNAME]/Library/Application Support/
  trademark/
    [APPNAME]/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/Users/[USERNAME]/Library/Application Support/
  [APPNAME]/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
