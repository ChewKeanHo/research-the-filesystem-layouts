# `/Users/[USERNAME]/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses user-specific configuration files (e.g. app libraries or
internal system files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
