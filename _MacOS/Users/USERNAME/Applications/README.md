# `Users/[USERNAME]/Applications`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all apps installed by a specific user without needing an
administrator (users with `wheel` permission) privilege. App procured via
App Stores under moderated control (e.g. parental control) by the user are
housed here automatically. User is allowed to install applications downloaded
elsewhere as long as the contents are signed and notarized by certified Apple
developers Program.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

You **CAN** place an app bundle (`.app`) entirely here. However, for stability
purposes, you **DEFINITELY MUST NOT** place or modify any files and folders
inside the bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to [Apple MacOS.app Bundle Filesystem](/_MacOS.app).
