# `/usr/share/man`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical, documentation manual files to extend the
OS' functionalities from *Critical & Minimal* stage to *Full Catalogue* stage.
This means it can operate in both `Multi-User` mode in BSD realm or `Full Mode`
in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages using FreeBSD's Ports Collections extension. All
workspace files' names and locations are registered by OS distributor.
Therefore, they are available consistently and uniformly across all the
machines.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Use `/usr/local/share` or
`${HOME}/[USERNAME]/.local/share` instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `man(1)` manual for specification.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/share/man/
  trademark/
    product/
      man1/
        amd64
        aarch64
        ...
      man2/
        amd64
        aarch64
        ...
      ...

OR

/usr/share/man/
  product/
    man1/
      amd64
      aarch64
      ...
    man2/
      amd64
      aarch64
      ...
    ...
```
