# `/root/Music`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses the `root` account's audio files. The initial design was
to let the user save all the music files in this directory and let the media
player only reads from here. Expected files are `.mp3`, `.m4a`, `.wav`, and etc.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ONLY** accessible `root` and OS administrators (users with
`wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.
