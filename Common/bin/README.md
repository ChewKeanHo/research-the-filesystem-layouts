# `/bin`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses command‑able programs and applications mapped to the
`$PATH` environment variable. Users can execute these programs easily using a
command (e.g., `date`) instead of the full file path (`/bin/date`).

Due to this directory's role in formulating the command list, it **MUST NOT**
contain any sub-directory. Each program or application must be uniquely named
exactly as the desired calling command.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The filename **MUST BE THE SAME** as desired command to call in terminal.
