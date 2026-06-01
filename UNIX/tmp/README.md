# `/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing temporary files and directories of an
operating system (OS) to function properly and minimally without any mounting
(e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for OS capabilities extension, performing self-rescue, or
straight up being operational in this resources constraint environment such as
but not limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

All files here are available to all users to create, read, update, and delete
based on the designated UNIX filesystem access permissions. **ONLY** all
sysadmins (user in `wheel` group), and `root` account has the overriding
capabilities.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

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
/tmp/
  trademark/
    product/
      ...

OR

/tmp/
  product/
    ...
```
