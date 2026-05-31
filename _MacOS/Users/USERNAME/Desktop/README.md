# `/Users/[USERNAME]/Desktop`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's files displayable onto the Desktop (screen).
Hidden files by default are hidden unless the user configures it to be shown
explictly.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is part of the `local domain`.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
