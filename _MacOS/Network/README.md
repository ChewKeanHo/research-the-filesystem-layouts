# `/Network`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses the list of computers in the local area network
designed for network interactions and file server mounting purposes (e.g.
mounting a network drive into the `/Volumes` directory). When developing an app,
one **MUST** always assume that files on any volume other than the boot volume
could be located on a network elsewhere.

This directory is part of the `local domain`.

Only admin-privileged (`wheel`) users can access this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders here for
avoiding breakage.
