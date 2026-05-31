# `/User/[USERNAME]/Library/Preferences`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all app-specific preference files created
by the `NSUserDefaults` class or `CFPreferences` API specifically for this user.

App **MUST NOT** create files in this directory manually.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding any breakage (e.g. signed signature). Let the installed apps handle
it.
