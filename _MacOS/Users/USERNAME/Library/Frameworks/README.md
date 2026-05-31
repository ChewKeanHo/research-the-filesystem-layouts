# `/Users/[USERNAME]/Library/Frameworks`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses frameworks and plugin bundles shared by multiple apps.
They are also the frameworks the developer use to create both macOS and iOS
apps. Frameworks and plugins procured via App Stores by the user under moderated
control (e.g. parental control) are housed here automatically.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

You **CAN AND SHOULD** place or modify any files and folders manually.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to:

1. [Apple Framework Bundle Filesystem](/_MacOS.framework)
2. [Apple Plugin Bundle Filesystem](/_MacOS.bundle)
