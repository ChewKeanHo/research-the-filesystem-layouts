# `/Users/[USERNAME]/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non-user files (e.g. app libraries or internal system
files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
