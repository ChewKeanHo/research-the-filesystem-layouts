# `/Users/[USERNAME]/Library/Frameworks`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses frameworks and plugin bundles shared by multiple apps.
They are also the frameworks the developer use to create both macOS and iOS
apps. Frameworks and plugins procured via App Stores by the user under moderated
control (e.g. parental control) are housed here automatically.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.

You **CAN AND SHOULD** place the framework (`.framework`) and bundle (`.bundle`
or `.plugin`) here. However, You **DEFINITELY MUST NOT** modify anything inside
any bundle manually for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to:

1. [Apple Framework Bundle Filesystem](/_MacOS.framework)
2. [Apple Plugin Bundle Filesystem](/_MacOS.bundle)
