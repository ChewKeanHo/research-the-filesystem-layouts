# `share/zoneinfo`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses timezone configuration data files for use with the
`tzfile(5)` format. These files must be CPU‑architecture independent. This
directory is specific to `UNIX`‑based OSes (e.g. `FreeBSD`, `Linux`-based OSes);
otherwise it is left blank.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD `tzfile(5)` manual for specifications.

This is a specific directory structure with forming query using pathing
strategy as such:

```
share/zoneinfo/
  [NAME] -> /usr/share/zoneinfo/Etc/GMT/GMT{+-ZZ}
  ...
```
