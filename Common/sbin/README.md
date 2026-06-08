# `sbin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses command-able system administrative programs and
applications mapped to the `$PATH` environment variable when the user is `root`
account or an administrator (on `FreeBSD` and `Linux`-based OSes: user with
`wheel` permission). These Users can execute the programs and applications
easily using the command format (e.g. `restart`) instead of the default full
filepath format (`/sbin/restart`).

Unlike `/bin` directory counterparts, programs and applications housed here are
typically for OS maintenance and administrations purposes like power management,
system tools, servers, etc. When executed wrongly, these programs usually yield
nasty consequences including damaging the hardware.

Due to the role of formulating commands list, it **MUST NOT** contain any
sub-directory. Each program or application **MUST BE** uniquely named as
**THE SAME** desirable calling command.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The filename **MUST BE THE SAME** as desired command to call in terminal.
