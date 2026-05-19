# `/Volumes`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all the mounted filesystems from local devices
(e.g. USB drive) and from network (`/Network`). When developing an app, one
**MUST** always assume that files on any volume other than the boot volume could
be located on a network elsewhere.

This directory is part of the `local domain`.

Everyone can access this directory except otherwise blocked explictly.

You can place, modify, update, or delete any files and folders here whenever
permitted.
