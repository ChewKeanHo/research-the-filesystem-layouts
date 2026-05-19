# `[APPNAME].app`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is an Apple's `MacOS` app bundle filesystem structure. A single app is a
project of its own. For `MacOS`, this is a clean directory having only a single
`Contents/` directory housing the actual app's contents.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Below is
a hybrid merged from `Mac OS X` (`MacOS` predecessor) and `MacOS`) itself.

Each app **MUST** have the `.app` file extension for identification.

```
[APPNAME].app
  Contents/
    [APPNAME].icns                  # (Required) app's ".icn" icon file.
    Info.plist                      # (Required) app's metadata.
    embedded.provisionprofile       # (Required) app's provisioning profile.
    Frameworks/
        [FRAMEWORKNAME].framework/  # app's externally added frameworks.
        ...
    Helpers/                        # app's help tools.
        README.txt
        ...
    MacOS/                          # (Required) app's executables directory.
      [APPNAME]                     # (Required) app's executable entry point.
      [APPNAME]-help                # an app's executable help app.
      [APPNAME]-utilities           # an app's other executable app.
      ...
    PlugIns/
        [PLUGIN].bundle/            # app's externally added plugin bundles.
        ...
    Resources/                      # (Required) app's resources directory.
      PrivacyInfo.xcprivacy         # (Required) app's privacy manifest file.
      Sounds/
        intro.wav
        ...
      Images/
        banner.avif
        ...
      en.lproj/                     # organized localized resources
          InfoPlist.strings
          Localizable.strings
          ...
          Images/                   # resources specific to this localization
            logo.avif
            ...
      jp.lproj/                     # organized localized resources
          InfoPlist.strings
          Localizable.strings
          ...
          Images/                   # resources specific to this localization
            logo.avif
            ...
```
