# `[APPNAME].app/Contents/Frameworks`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's many dependencies specifically Apple complied
Frameworks. A single framework can have various resource files such as but not
limited to statically complied library files, graphics, etc.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer to [Apple MacOS Framework Bundle Filesystem](/_MacOS.framework).
