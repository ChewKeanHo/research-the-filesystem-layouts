# `/Network`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses the list of computers in the local area network. For
file server, mount it from here into the `/Volume` directory. When developing
an app, always assume that files on any volume other than the boot volume could
be located on a network-based server.
