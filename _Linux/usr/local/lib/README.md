# `/usr/local/lib`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user's system-wide, custom supplied,
non-critical, library files (e.g. C object artifact files) to extend the
operating system (OS)'s functionalities from *Full Catalogue* stage to
*Complete* stage. This means it can operate in both `Multi-User` mode in BSD
realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities to its complete form by isolating
OS distributor's packages away from user's system-wide OS customizations. These
customizations, in theory, only specific to this machine instance.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD** place your own system-wide custom library files here.

In many Linux OSes like SystemD and UAPI, this directory is
**DEPRECATED AND REMOVED** in favor of using `/home/[USERNAME]/.local/lib`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/local/lib/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/usr/local/lib/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
