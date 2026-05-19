# `/Users/[USERNAME]/Public`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's public sharable files. The initial design was to
let the user houses all the public sharable files in this directory and let the
file sharing servers like SAMBA or SSHFS to read and write from here.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
