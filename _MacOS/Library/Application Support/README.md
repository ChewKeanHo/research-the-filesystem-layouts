# `/Library/Application Support`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses app data except those associated with user's documents.
Files like app-created data files, configuration files, templates, or other
fixed or modifiable resources managed by an app.

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

All users should be able to read and use the contents from this directory except
when being restricted. Only admin-privileged (`wheel`) users and system-level
installed apps can modify or delete contents in this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding breakage. Let the installed apps from Apple's AppStore handle it.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

All libraries here are POSIX compliant registered libraries that are usable
across all UNIX and UNIX-like OSes.

It is a practice to house the files using `trademark` and `[APPNAME]`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/Library/Application Support/
  trademark/
    [APPNAME]/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/Library/Application Support/
  [APPNAME]/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
