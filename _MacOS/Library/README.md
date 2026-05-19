# `/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non-user files (e.g. app libraries or internal system
files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

All users should be able to read the contents from this directory except when
being restricted. Only admin-privileged (`wheel`) users and system-level
installed apps can modify or delete contents in this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding breakage. Let the installed apps handle it.
