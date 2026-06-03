# `share/zoneinfo`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent `tzfile` timezone
configuration data files. These files are accessible by various programs,
applications, and development project for an unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD `tzfile(5)` manual for specifications.

This is a specific directory structure with forming query using pathing
strategy as such:

```
share/zoneinfo/
  [NAME] -> /usr/share/zoneinfo/Etc/GMT/GMT{+-ZZ}
  ...

OR

share/zoneinfo/
  [NAME] -> /usr/share/zoneinfo/Etc/GMT/GMT{+-ZZ}
  ...
```
