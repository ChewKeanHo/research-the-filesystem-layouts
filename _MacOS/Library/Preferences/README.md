# `/Library/Preferences`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all app-specific preference files created
by the `NSUserDefaults` class or `CFPreferences` API.

App **MUST NOT** create files in this directory manually.

This directory is part of the `local domain`.

All users should be able to read and use the contents from this directory except
when being restricted. Only admin-privileged (`wheel`) users and system-level
installed apps can modify or delete contents in this directory.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding any breakage (signed signature). Let the installed apps from
Apple's AppStore handle it.
