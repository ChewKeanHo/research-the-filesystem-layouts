# `/usr/share/factory`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, factory default configurations and data files to extend
the OS' functionalities from *Critical & Minimal* stage to *Full Catalogue*
stage. This means it can operate in both `Multi-User` mode in BSD realm or
`Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All files names and locations are registered by
OS distributor. Therefore, they are available consistently and uniformly across
all the machines.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Keep in mind that everything in this directory
resets the root filesystems to factory default settings.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy reduces the configuration
complexities and making maintainability easier by just keeping 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
/usr/share/factory/
  var/
    trademark/
      product1/
        program.pdf
        program.txt
        program.1
        ...
      product2/
        program.pdf
        program.txt
        program.1
        ...
    ...
  etc/
    trademark/
      product/
        settings.d/
          setting1.conf
          setting2.conf
          ...
  ...

# OR

/usr/share/factory/
  var/
    product1/
      program.pdf
      program.txt
      program.1
      ...
    product2/
      program.pdf
      program.txt
      program.1
      ...
    ...
  etc/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...
  ...
```
