# `/home/[USERNAME]/Videos`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's video files. The initial design was to let the
user houses all the movies and videos in this directory and let the media player
streams only from here. Expected files are `.mp4`, `.mkv`, `.ogg`, etc.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
