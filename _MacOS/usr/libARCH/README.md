# `/usr/lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, non-critical CPU architecture specific library files
(e.g. C object artifact files) to extend the OS' functionalities from
*Critical & Minimal* stage to *Full Catalogue* stage. This means it can operate
in both `Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All library files' names and locations are
registered by OS distributor. Therefore, they are available consistently and
uniformly across all the machines.

All files here are available to all users.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS in any way. Use `/usr/local/lib[ARCH]` instead.

Also, if this directory is used, you **SHOULD ALWAYS** utilize the main
`/usr/lib` directory at all time. Library files can be named with the
`[COMPILER]-[OS]-[ARCH]` triplet for identifications over there.

This directory pattern is considered old and obselete when `x86` CPU
architecture was migrated completely from `i386` to `amd64` architectures.
During the migrations, both architectures are required to exist so this pattern
was invented. Use unless absolutely necessary and only only place your own
system-wide custom CPU architecture specific library files here (e.g. `arm64`
library files on an `amd64` OS where they are used for cross-compilation).

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples for ARCH is `32` (32-bit on 64-bit OS):

```
/usr/lib32/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/usr/lib32/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
