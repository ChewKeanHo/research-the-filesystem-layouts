# `/Users/[USERNAME]/Sites`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's published personal web pages. The web pages
**MUST** be served by a web server and `Web Sharing` **MUST** be enabled.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.
