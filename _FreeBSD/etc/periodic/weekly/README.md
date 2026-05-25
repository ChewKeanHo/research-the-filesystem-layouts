# `/etc/periodic/weekly`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s cron weekly scheduler's
configuration files using the `.d` configuration directory pattern where 1 file
is 1 cron file. It can operate minimally without any mounting (e.g. `/usr` is
not mounted or absent). This means it can operate in `Single-User` mode in BSD
realm or `Emergency Mode` in Linux realm.

Note that the configuration in this `weekly` directory is similar to:

```
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * user-name command to be executed
0    2  *  *  6 root /bin/printf "%s\n" "periodic weekly"
```

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

FreeBSD practices the use of `/usr/local/etc` so use
`/usr/local/etc/periodic/weekly` instead. Therefore, generally, you
**SHOULD NOT** place or modify the configuration files that are very critical to
the OS.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You **MUST** refer to `cron(8)` and `periodic(8)` manual for the configuration
file format.

Generally, it is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/etc/periodic/weekly/
  trademark-product-task1.cron
  trademark-product-task2.cron
  ...

OR

/etc/periodic/weekly/
  product-task1.cron
  product-task2.cron
  ...
```
