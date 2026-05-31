# `[PLUGINNAME].bundle/Contents/Resources`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a plugin bundle's language independent or generalized
resources files. This is the usual workspaces an plugin bundle developer works
in.

Localized language directory is organized using the `[LANG].lproj` sub-directory
and have their assets summoned via Apple Foundation APIs.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

For localization, the sub-directory **MUST** be named as `[LANG].lproj` pattern
like `en.lproj` for English and `jp.lproj` for Japanese. Any contents therein
are specifically for that language.

Content files can be anything used by the main executable like libraries files,
sound files, interpretable source codes, image files, icon files,
internationalization datasets, etc.

Otherwise, it is entirely upto the app developer and the Apple's XCode editor
used to structure this directory.
