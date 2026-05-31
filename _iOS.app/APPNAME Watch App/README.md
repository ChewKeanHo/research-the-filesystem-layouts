# `[APPNAME].app/[APPNAME] Watch App`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's integrated Apple Watch device `WatchOS` "bundle".
Unlike conventional bundles, this watch app is closely associated into an iOS
app but acting as an independent target. It has its own structure and can have
various resource files such as but not limited to statically complied library
files, graphics, etc.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Depending on XCode version, some WatchOS target addition may create its own
single main entry point executable. **DO DELETE IT** as the entire app is using
iOS single main entry point executable instead.

Likewise, `WatchOS` itself has its own set of:

* `ContentView` - `WatchOS` app's integrated control executable.
* `Assets`      - `WatchOS` app's graphical asset bundles.
* `Frameworks/` - `WatchOS` app's externally added frameworks.
* `PlugIns/`    - `WatchOS` app's externally added plugin bundles.

Code development for `WatchOS` lies within `ContentView`.
