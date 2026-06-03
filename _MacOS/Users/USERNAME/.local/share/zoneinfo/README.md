# `/Users/[USERNAME]/.local/share/zoneinfo`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing a single user's user-specific, user
supplied, non-critical, `tzfile` timezone configuration data files of an OS to
function properly. This means it can operate in `Multi-User` mode in BSD realm
or `Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Complete* stage to
*Personalized* stage achieving full per-user customization capabilities. All
payloads, filepaths, configurations, data, etc. are specific to this runtime
hardware and to the owning user.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to the owning user, `root` account, and OS
administrators (users with `wheel` permission) for create, read, update, and
delete operation.

In some `Linux`-based OSs notably SystemD-based, Red Hat, and Fedora; this
directory is heavily used as they shifted user-oriented dedicated software like
flatpak package manager (e.g. `$ flatpak --user install`) for achieving rootless
operation.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

In Microsoft `Windows`, this directory is inter-compatible with other UNIX and
UNIX-like OSes for localized software package management.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `tzfile(5)` manual for specifications.

This is a specific directory structure with forming query using pathing
strategy as such:

```
/Users/[USERNAME]/.local/share/zoneinfo/
  [NAME] -> /usr/share/zoneinfo/Etc/GMT/GMT{+-ZZ}
  ...

OR

/Users/[USERNAME]/.local/share/zoneinfo/
  [NAME] -> /usr/share/zoneinfo/Etc/GMT/GMT{+-ZZ}
  ...
```
