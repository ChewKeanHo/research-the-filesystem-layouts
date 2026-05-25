# `/usr/share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user's system-wide, custom supplied,
non-critical, document files (e.g. PDF, text README) to extend the operating
system (OS)'s functionalities from *Full Catalogue* stage to *Complete* stage.
This means it can operate in both `Multi-User` mode in BSD realm or `Full Mode`
in Linux realm.

The goal is to extend the OS' functionalities to its complete form by isolating
OS distributor's packages away from user's system-wide OS customizations. These
customizations, in theory, only specific to this machine instance.

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

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/share/doc/
  trademark/
    product1/
      program.pdf
      program.txt
      ...
    product2/
      program.pdf
      program.txt
      ...
    ...

# OR

/usr/share/doc/
  product1/
    program.pdf
    program.txt
    ...
  product2/
    program.pdf
    program.txt
    ...
  ...
```
