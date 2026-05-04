# `/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non-user files (e.g. app libraries or internal system
files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain` only admin-privileged (`wheel`)
users can modify or delete.
