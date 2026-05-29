# `/root/Desktop`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's files displayable onto the Desktop (screen).
Hidden files by default are hidden unless the user configures it to be shown
explictly.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

**Only `root` and administrators (users with `wheel` permission) can access the
directory**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, unless absolute necessary, you **SHOULD NOT** place anything here
**UNLESS** you are the OS distributor. This is to avoid any conflict with the
upstream's registries that will break the OS in any way. Use `/home/[USERNAME]`
instead.
