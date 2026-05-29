# `/lib[ARCH]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing operating system (OS)'s system-wide,
OS distributor supplied, critical CPU architecture specific library files
(e.g. C object artifact files) to function properly and minimally without any
mounting (e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode for BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for functionalities extension, performing self-rescue, or
straight up operational in resources constraint environment such as but not
limited to OpenWRT embedded router.

This directory pattern is considered old and obselete when `x86` CPU
architecture was migrated completely from `i386` to `amd64` architectures.
During the migrations, both architectures are required to exist so this pattern
was invented. Use unless absolutely necessary and only only place your own
system-wide custom CPU architecture specific library files here (e.g. `arm64`
library files on an `amd64` OS where they are used for cross-compilation).

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer seeing performance compromise between
`/` and `/usr`, this directory is being symbolic linked to `/usr/lib[ARCH]`
instead; unifying both directories. This reduces the separation complexities
while simplifying the package managements to target `/usr/lib[ARCH]` only.

If this directory is used, you **SHOULD ALWAYS** utilize the main `/lib[ARCH]`
directory at all time. Library files can be named with the
`[COMPILER]-[OS]-[ARCH]` triplet for identifications over there.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD ONLY** place libraries that are very critical at early
booting stage without conflicting with existing libraries. In the case of
`/lib[ARCH]` being symbolic linked to `/usr/lib[ARCH]`, you **MUST NOT** place
anything here and use `/usr/lib[ARCH]` exclusively instead.




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
