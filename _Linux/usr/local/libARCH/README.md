# `/usr/local/lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing user's system-wide, custom supplied,
non-critical, CPU architecture specific library files (e.g. C object artifact
files) to extend the operating system (OS)'s functionalities from
*Full Catalogue* stage to *Complete* stage. This means it can operate in both
`Multi-User` mode in BSD realm or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities to its complete form by isolating
OS distributor's packages away from user's system-wide OS customizations. These
customizations, in theory, only specific to this machine instance.

This directory pattern is considered old and obselete when `x86` CPU
architecture was migrated completely from `i386` to `amd64` architectures.
During the migrations, both architectures are required to exist so this pattern
was invented. Use unless absolutely necessary and only only place your own
system-wide custom CPU architecture specific library files here (e.g. `arm64`
library files on an `amd64` OS where they are used for cross-compilation).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD ALWAYS** utilize the main `/usr/local/lib` directory at
all time. Library files can be named with the `[COMPILER]-[OS]-[ARCH]` triplet
for identifications over there.

In many Linux OSes like SystemD and UAPI, this directory is
**DEPRECATED AND REMOVED** in favor of using `/home/[USERNAME]/.local/lib[ARCH]`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples for ARCH is `32` (32-bit on 64-bit OS):

```
/usr/local/lib32/
  trademark/
    product/
      lib1.a
      lib1_freebsd-amd64.a
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/usr/local/lib32/
  product/
    lib1.a
    lib1_freebsd-amd64.a
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
