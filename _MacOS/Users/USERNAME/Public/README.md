# `/Users/[USERNAME]/Public`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's public sharable files. The initial design was to
let the user houses all the public sharable files in this directory and let the
file sharing servers like SAMBA or SSHFS to read and write from here.

This directory is part of the `local domain`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by any user for `read` permission. Only the owning
user, `root`, and OS administrators (users with `wheel permission) can `create`,
`update`, and `delete` content.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
