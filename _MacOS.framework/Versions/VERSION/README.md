# `[FRAMEWORKNAME].framework/Versions/[VERSION]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a specific version of framework's resources files and its
single main entry point executable. This is the usual workspaces a framework
developer works in where it uses and summon the required assets from this
directory for that specific version. These versioned controlled directories are
made available for external to perform backward-compatible usabilities.
Framework developer choose a version and symlinked as `Current` to facilitate
the latest and current version for external to use.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Each
`[VERSION]` has its own `Info.plist`, `[FRAMEWORKNAME]` single main entry point
executable, `[FRAMEWORKNAME].icns`, `Frameworks`, `PlugIns`, `Helpers`,
`Resources` and `PrivacyInfo.xcprivacy`.

Other content files can be anything used by the main executable like libraries
files, sound files, interpretable source codes, image files, icon files,
internationalization datasets, etc.

When needed, refer back [Apple MacOS Framework Bundle Filesystem](/_MacOS.framework)
for its filesystem structure mapping once more.
