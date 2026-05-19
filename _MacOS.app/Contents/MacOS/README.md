# `[APPNAME].app/Contents/MacOS`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's executables **including the single main entry
point**. It usually **ONLY houses a single main executable** but the app
developer can additional executables (e.g. helper, utilities) for facilitating
more command lines functionalities. In short, this is similar to `bin` directory
from UNIX filesystems hierarchy standards convention.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The single and main executable is named exactly as the `[APPNAME]` for the OS
to uniformly summon the app via this path:

```
[APPNAME].app/Contents/MacOS/[APPNAME]
```

Other executables' name **MUST BE THE SAME** as the desired commands
respectively without conflicting with the single main executable.
