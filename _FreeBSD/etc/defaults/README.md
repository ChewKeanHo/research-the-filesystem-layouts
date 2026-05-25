# `/etc/defaults`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing default configuration files for restoration
purposes.

The goal is plain simple: factory-reset a certain configuration file when it is
always available.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD NOT** edit anything here. Only read and overwrite the
runtime version for restoration.




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
/etc/defaults/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/etc/defaults/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
