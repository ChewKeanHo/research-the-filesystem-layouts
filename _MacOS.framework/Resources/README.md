# `[FRAMEWORKNAME].framework/Resources`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This "directory" is a symbolic link pointing to `Version/Current/Resources`'s
resources directory inside the framework itself. Its existence is mainly for
facilitating default use. Once created, this link file is rarely touched or
modified.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).
