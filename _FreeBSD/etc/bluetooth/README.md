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




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `bluetooth` manual for specifications.

Generally, it is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Moreover, the use of `.d` configuration directory strategy also reduces the
configuration complexities and making maintainability easier by just updating 1
configuration per file. The program would loop through the directory and parse
everything.

Here are the examples:

```
/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
