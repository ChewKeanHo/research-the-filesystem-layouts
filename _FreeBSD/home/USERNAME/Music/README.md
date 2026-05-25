# `/home/[USERNAME]/Music`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's audio files. The initial design was to let the
user save all the music files in this directory and let the media player only
reads from here. Expected files are `.mp3`, `.m4a`, `.wav`, and etc.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
