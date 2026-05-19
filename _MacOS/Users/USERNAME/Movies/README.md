# `/Users/[USERNAME]/Movies`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's video files. The initial design was to let the
user houses all the movies and videos in this directory and let the media player
streams only from here. Expected files are `.mp4`, `.mkv`, `.ogg`, etc.

Only admin-privileged (`wheel`) and owning users can access this directory.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.
