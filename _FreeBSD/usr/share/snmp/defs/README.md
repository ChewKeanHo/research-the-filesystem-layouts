# `/usr/share/snmp/defs`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical, SNMP tree definition files to extend the
OS' functionalities from *Critical & Minimal* stage to *Full Catalogue* stage.
This means it can operate in both `Multi-User` mode in BSD realm or `Full Mode`
in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages using FreeBSD's Ports Collections extension. All
workspace files' names and locations are registered by OS distributor.
Therefore, they are available consistently and uniformly across all the
machines.

All files here are generally available to all users but can be invisible based
on FreeBSD's Ports configurations.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Use `/usr/local/share` or
`${HOME}/[USERNAME]/.local/share` instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/share/snmp/defs/
  trademark/
    product/
      setting1.def
      setting2.def
      ...

OR

/usr/share/snmp/defs/
  product/
    setting1.def
    setting2.def
    ...
```
