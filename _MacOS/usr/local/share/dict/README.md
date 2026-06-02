# `/usr/local/share/dict`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, user supplied, non-critical,
CPU architecture independent words list files of an OS to function properly.
This means it can operate in `Multi-User` mode in BSD realm or `Full Mode` in
Linux realm.

The goal is to expand the OS' functionalities from *Full Catalogue* stage to
*Complete* stage achieving full user-customized system-wide capabilities. All
payloads, filepaths, configurations, data, etc. are specific to this runtime
hardware and is completely customizable by system administrator (user with
`wheel` privilege).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD** place your file here for all users. If you want only
for a specific user, use `${HOME}/[USERNAME]/.local/share` instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `look(1)` manual for specifications.

Known list files are like:

```
/usr/local/share/dict/
  freebsd           # FreeBSD wording, jargons, etc.
  README
  propernames
  web2              # words from Webster's Second International
  web2a
  words
```
