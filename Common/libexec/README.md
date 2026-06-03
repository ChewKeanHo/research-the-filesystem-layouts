# `libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non-commandable programs and applications. User **MUST**
execute the programs and applications using the full filepath. Any executable be
it a compiled application program artifact or a shell script can be placed here.

The directory is intentionally designed to house internal executables (e.g.
server) or subroutine scripts called by other programs (e.g. an init, another
program or application, a scheduler). Hence, they are not mapped to the
commands list.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The filename **MUST BE THE SAME** as desired command to call in terminal.
