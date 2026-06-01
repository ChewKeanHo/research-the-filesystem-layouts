# `/Users/[USERNAME]/Library/Preferences`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all app-specific preference files created
by the `NSUserDefaults` class or `CFPreferences` API specifically for this user.

App **MUST NOT** create files in this directory manually.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding any breakage (e.g. signed signature). Let the installed apps handle
it.
