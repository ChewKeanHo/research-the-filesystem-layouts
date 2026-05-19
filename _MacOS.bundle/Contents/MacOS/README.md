# `[PLUGINNAME].bundle/Contents/MacOS`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses one or more plugin bundle's executables. In short, this is
similar to `bin` directory from UNIX filesystems hierarchy standards convention.

Unlike an `.app` bundle, there is no single main executable to maintain.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Executables' name **MUST BE THE SAME** as the desired commands respectively
without conflicting with the single main executable.
