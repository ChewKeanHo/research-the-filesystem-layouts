# `Users/[USERNAME]/Applications`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all apps installed by a specific user without needing
an administrator privilege (users with `wheel` permission). App procured via
App Stores under moderated control (e.g. parental control) by the user are
housed here automatically.

This directory is part of the `local domain`.

Only admin-privileged (`wheel`) and owning users can access this directory.

You **CAN** place an app bundle (`.app`) entirely here. However, for stability
purposes, you **DEFINITELY MUST NOT** place or modify any files and folders
inside the bundle for avoiding breakage.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to [Apple MacOS.app Bundle Filesystem](/_MacOS.app).
