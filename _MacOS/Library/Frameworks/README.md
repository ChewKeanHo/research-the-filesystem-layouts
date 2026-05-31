# `/Library/Frameworks`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses frameworks and plugin bundles shared by multiple apps.
They are also the frameworks the developer use to create both macOS and iOS
apps. Frameworks and plugins procured via App Stores by the user are housed here
automatically.

This directory is part of the `local domain`.

All users should be able to read and use the contents from this directory except
when being restricted. Only admin-privileged (`wheel`) users and system-level
installed apps can modify or delete contents in this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding any breakage (signed signature). Let the installed frameworks from
Apple's AppStore handle it.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to:

1. [Apple Framework Bundle Filesystem](/_MacOS.framework)
2. [Apple Plugin Bundle Filesystem](/_MacOS.bundle)
