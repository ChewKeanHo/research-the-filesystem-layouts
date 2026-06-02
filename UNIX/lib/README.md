# `/lib`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical library files used by critical
library files (e.g compiled linkable object files) of an operating system (OS)
to function properly and minimally without any mounting (e.g. `/usr` is not
mounted or absent). This means it can operate in `Single-User` mode in BSD realm
or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for OS capabilities extension, performing self-rescue, or
straight up being operational in this resources constraint environment such as
but not limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In some `Linux`-based OSes like Oracle's Solaris (first to transform back in
2012) and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is
always being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, `/usr/lib` directory is being symbolic linked to
`/lib` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/lib` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/lib` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way. Use `/usr/local/lib` or
`${HOME}/[USERNAME]/.local/lib` instead. In the case of `/lib` being
symbolically linked from `/usr/lib`, you **MUST** place the content in
`/usr/lib` instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/lib/
  trademark/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/lib/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```
