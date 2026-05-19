# `[FRAMEWORKNAME].framework/Versions/Current`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This "directory" houses the current version of framework's resources files. It
is a symbolic link with relative path pointing to the specific version in the
same directory (e.g. `A` or `v1.0.0`). This symlink is made available for
external to always use the current latest contents rather than a specific
version.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).
