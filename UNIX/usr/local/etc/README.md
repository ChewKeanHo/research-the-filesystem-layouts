# `/usr/local/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, user supplied, non-critical
configuration files of an operating system (OS) to function properly. This means
it can operate in `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

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

In many `Linux`-based OSes, they do not practice using this directory but still
honoring it. Instead all files are unified under `/etc` directory. Some like
Red Hat Linux is still using this directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD** place your file here for all users. If you want only
for a specific user, use `${HOME}/[USERNAME]/.local/etc` instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy also reduces the configuration
complexities and making maintainability easier by just updating 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
/usr/local/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/usr/local/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
