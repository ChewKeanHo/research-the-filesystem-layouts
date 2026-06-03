# `/etc/bluetooth`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s bluetooth input/output
(IO) configuration files for enabling IO function properly and as expected. It
can operate minimally without any mounting (e.g. `/usr` is not mounted or
absent). This means it can operate in `Single-User` mode in BSD realm or
`Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

For FreeBSD, it has the following notable configuration files that can make or
break the OS. Some already deployed the `.d` directory configurations strategy
so their existences are optional. Known configurations are:

```
/etc/bluetooth/
  hcsecd.conf  # HCI security daemon configuration file.
  hosts        # bluetooth host database file.
  protocols    # bluetooth Protocol/Service Multiplexor (PSM) names and numbers.
```

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `bluetooth` manual for specifications.
