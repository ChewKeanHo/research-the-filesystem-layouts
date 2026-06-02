# `/usr/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, operating system (OS)
distributor supplied, non-critical gaming programs and applications of an OS to
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

In some `Linux`-based OSes like Oracle's Solaris (first to transform back in
2012) and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is
always being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, `/usr/bin` directory is being symbolic linked to
`/bin` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/bin` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/bin` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The filename **MUST BE THE SAME** as desired command to call in terminal.
