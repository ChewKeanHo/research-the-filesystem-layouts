# `/usr/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, operating system (OS)
distributor supplied, non-critical temporary files and directory workspace of an
OS to function properly. This means it can operate in `Multi-User` mode in BSD
realm or `Full Mode` in Linux realm.

The goal is to expand the OS' functionalities from *Minimum & Critical* stage to
*Full Catalogue* stage achieving full distributor-grade warranted capabilities.
All payloads, filepaths, configurations, data, etc. are strictly registered by
the OS distributor for achieving uniformity and consistency across ALL hardware
(fleet management).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to create, read, update, and delete
based on the designated UNIX filesystem access permissions. **ONLY** all
sysadmins (user in `wheel` group), and `root` account has the overriding
capabilities.

In many `Linux`-based OSes, this directory is unused. Only Red Hat Linux and
Fedora are using it and symlinked from `/tmp` directory.

In FreeBSD, this directory is unused.

In Apple `MacOS`, this directory is unused.

Generally, you **SHOULD ONLY** place files that requires temporary space for
operations here. It is **HIGHLY RECOMMENDED** to remove all the files before and
after use for preventing any possible data poisoning occurances.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/tmp/
  trademark/
    product/
      ...

OR

/usr/tmp/
  product/
    ...
```
