# `/User/[USERNAME]/Library/Preferences`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all app-specific preference files created
by the `NSUserDefaults` class or `CFPreferences` API specific for this user.

App **MUST NOT** create files in this directory manually.

This directory is part of the `local domain`.

Only admin-privileged (`wheel`) and owning users can access this directory.

You **CAN AND SHOULD** place or modify any files and folders manually.
