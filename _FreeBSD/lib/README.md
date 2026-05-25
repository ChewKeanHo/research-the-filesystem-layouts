# `/lib`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical libraries used by critical
programs and applications of an operating system (OS) to function properly and
minimally without any mounting (e.g. `/usr` is not mounted or absent). This
means it can operate in `Single-User` mode.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for functionalities extension, performing self-rescue, or
straight up operational in resources constraint environment such as but not
limited to OpenWRT embedded router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer seeing performance compromise between
`/` and `/usr`, this directory is being symbolic linked to `/usr/lib` instead;
unifying both directories. This reduces the separation complexities while
simplifying the package managements to target `/usr/lib` only. **FreeBSD
however, have not seen to perform such implementation yet likely for backward
compatibility purposes.**

Generally, you **SHOULD ONLY** place libraries that are very critical at early
booting stage without conflicting with existing libraries. In the case of
`/lib` being symbolic linked to `/usr/lib`, you **MUST NOT** place anything here
and use `/usr/lib` exclusively instead.




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
