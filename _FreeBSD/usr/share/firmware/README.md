# `/usr/share/firmware`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, operating system (OS)
distributor supplied, non-critical, firmware image data files of an OS to
function properly. This means it can operate in `Multi-User` mode in BSD realm
or `Full Mode` in Linux realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All payloads, filepaths, configurations, data,
etc. are strictly registered by the OS distributor for achieving uniformity
and consistency across ALL hardware (fleet management).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In FreeBSD, the following files are available:

```
/usr/share/misc/
  ascii       # chart of the ASCII codepoints.
  flowers     # the meanings of flowers.
  magic       # magic numbers used by file(1).
  termcap     # terminal characteristics database; see termcap(5).
```

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way. Use
`/usr/local/share/firmware` or `${HOME}/[USERNAME]/.local/share/firmware`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/usr/share/firmware/
  trademark/
    product/
      device.bin
      cpuX.bin
      board.bin
      ...

OR

/usr/share/firmware/
  product/
    device.bin
    cpuX.bin
    board.bin
    ...
```
