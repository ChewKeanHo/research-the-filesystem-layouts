# `/usr/share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical document files (e.g. man pages) to extend
the OS' functionalities from *Critical & Minimal* stage to *Full Catalogue*
stage. This means it can operate in both `Multi-User` mode in BSD realm or
`Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All document files' names and locations are
registered by OS distributor. Therefore, they are available consistently and
uniformly across all the machines.

All files here are available to all users.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Use `/usr/local/share/doc` or
`${HOME}/[USERNAME]/.local/share/doc` instead.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




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
      program.1
      ...
    product2/
      program.pdf
      program.txt
      program.1
      ...
    ...

# OR

/usr/share/doc/
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
```
