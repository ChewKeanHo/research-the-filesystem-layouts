# `[PLUGINNAME].bundle/Contents/Resources/[LANG].lproj`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a plugin bundle's single language-specific resources
files. This is the usual workspaces an plugin bundle developer works in.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The directory **MUST** be named as `[LANG].lproj` pattern like `en.lproj` for
English and `jp.lproj` for Japanese.

Content files can be anything used by the main executable like libraries files,
sound files, interpretable source codes, image files, icon files,
internationalization datasets, etc.

Otherwise, it is entirely upto the app developer and the Apple's XCode editor
used to structure this directory.
