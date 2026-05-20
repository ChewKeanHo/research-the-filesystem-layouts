# `[PLUGINNAME].app/[LANG].lproj`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an `iOS` plugin bundle's single language-specific
resources files. This is the usual workspaces an app developer works in where it
uses and summon the required assets from this directory for one specific
language.

If you are developing using XCode, then you may structure your content
accordingly.

Since `iOS` is **DISALLOWED AND PROHIBITED** to create a framework bundle on
production, plugin bundle is only used in XCode development as app imported
module.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The directory **MUST** be named as `[LANG].lproj` pattern like `en.lproj` for
English and `jp.lproj` for Japanese.

Content files can be anything used by the main executable like libraries files,
sound files, interpretable source codes, image files, icon files,
internationalization datasets, etc.

Otherwise, it is entirely upto the app developer and the Apple's XCode editor
used to structure this directory.
