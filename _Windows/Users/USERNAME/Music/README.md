# `[DRIVE]\Users\[USERNAME]\Music`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's audio files. The initial design was to let the
user save all the music files in this directory and let the media player only
reads from here. Expected files are `.mp3`, `.m4a`, `.wav`, and etc.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
