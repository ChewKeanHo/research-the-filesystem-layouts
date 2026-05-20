# `/Library/Caches`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses re-creatable and performance-improving files. The apps
are generally responsible for their own caches files including creating and
removing them after use for avoiding data poisoning.

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

The operating system (OS) can delete this directory when it is very low on disk
space and the app is not running.

Backup restoration is not necessarily means this directory can be erased.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding breakage. Let the installed apps from Apple's AppStore handle it.

The content are not backed up by iTunes and iCloud.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `[APPNAME]`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/Library/Caches/
  trademark/
    [APPNAME]/
      lib1.dat
      lib1_freebsd-amd64.dat
      kernel8.dat
      kernel8_freebsd-amd64.dat
      ...

# OR

/Library/Caches/
  [APPNAME]/
    lib1.dat
    lib1_freebsd-amd64.dat
    kernel8.dat
    kernel8_freebsd-amd64.dat
    ...
```
