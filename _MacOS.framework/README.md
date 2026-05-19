# `[FRAMEWORKNAME].framework`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is an Apple's `MacOS` framework bundle filesystem structure. A single
framework is a project of its own. For `MacOS`, this is a clean,
version-controlled directories system with clever use of symbolic links.

While being a framework, there is a single main entry point executable govening
the entire framework named as `[FRAMEWORKNAME]`. At the root directory, this
`[FRAMEWORKNAME]` is symlinked to the `Current/` version of the
`[FRAMEWORKNAME]`. Once the symbolic link is created, it is rarely touched
throughout the development cycle.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Below is
`Mac OS X`'s structure, the `MacOS` predecessor.

Each framework **MUST** have the `.framework` file extension for identification.

Basically, a framework is a version-controlled directories of resources files
where:

1. External calls `[FRAMEWORKNAME].framework/[FRAMEWORKNAME]` and
   `[FRAMEWORKNAME].framework/Resources` symlinked to
   `[FRAMEWORKNAME].framework/Versions/Current` for accessing the current
   version of the contents.
2. The `[FRAMEWORKNAME].framework/Versions/Current` is then symlinked to a
   specific version inside the `[FRAMEWORKNAME].framework/Versions/` directory.
   In the following example, it is pointing to `v1.0.0`.
3. Therefore, the framework is version-controlled and the developer only needs
   to work inside the `Versions/` directory.
4. Duly noted that the `Info.plist` is inside `Versions/[VERSION]/Resources/`
   directory instead of the bundle root directory.
5. While unrestricted, external can directly access a specific version of the
   resources directly by `[FRAMEWORKNAME].framework/Versions/[VERSION]/...`
   pathing. **This is ESPECIALLY GOOD PRACTICE for de-coupling a framework's
   independent development progress from the external project**.

```
[FRAMEWORKNAME].framework/
   [FRAMEWORKNAME]  -> Versions/Current/[FRAMEWORKNAME] # (Required) framework's entry point.
   Resources        -> Versions/Current/Resources       # (Required) framework's entry point.
   Versions/
      Current       -> v1.0.0     # (Required) framework's current version.
      v1.0.0/                     # (Required) a specific version of resources.
         [FRAMEWORKNAME]          # (Required) a specific version of framework's entry point.
         Frameworks/
            [OTHER_FRAMEWORKNAME].framework/    # externally added frameworks.
            ...
         PlugIns/
            [OTHER_FRAMEWORKNAME].bundle/       # externally added plugin bundles.
            ...
         Helpers/                               # help app or help tools
            README.txt
            ...
         Resources/
            Info.plist             # (Required) framework's configuration and metadata.
            [FRAMEWORKNAME].icns   # (Required) framework's ".icn" icon file.
            PrivacyInfo.xcprivacy  # (Required) framework's privacy manifest file.
            Headers/
              MyHeader.h
            Sounds/
              intro.wav
              ...
            Images/
              banner.avif
              ...
            en.lproj/              # organized localized resources
               InfoPlist.strings
               Localizable.strings
               ...
               Images/             # resources specific to this localization
                 logo.avif
                 ...
            jp.lproj/
               InfoPlist.strings
               Localizable.strings
               ...
               Images/             # resources specific to this localization
                 logo.avif
                 ...
            ...
```
