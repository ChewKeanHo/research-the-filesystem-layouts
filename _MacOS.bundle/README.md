# `[PLUGINNAME].bundle`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is an Apple's `MacOS` plugin bundle filesystem structure. A single plugin
is a project of its own. For `MacOS`, this is a clean directory having only a
single `Contents/` directory housing the actual app's contents. Unlike app
bundles, plugin **DOES NOT** have a single main entry executable to maintain.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Below is a
hybrid merged from `Mac OS X` (`MacOS` predecessor) and `MacOS`) itself.

Each app **MUST** have the `.bundle` or `.plugin` file extension for
identification.

```
[APPNAME].bundle
  Contents/
    [APPNAME].icns                  # (Required) plugin's ".icn" icon file.
    Info.plist                      # (Required) plugin's metadata.
    embedded.provisionprofile       # (Required) plugin's provisioning profile.
    Frameworks/
        [FRAMEWORKNAME].framework/  # plugin's externally added frameworks.
        ...
    Helpers/                        # plugin's help tools.
        README.txt
        ...
    MacOS/                          # plugin's executables directory.
      [APPNAME]                     # an plugin's executable app.
      [APPNAME]-help                # an plugin's executable help app.
      [APPNAME]-utilities           # an plugin's other executables app.
      ...
    PlugIns/
        [PLUGIN].bundle/            # plugin's externally added plugin bundles.
        ...
    Resources/                      # (Required) plugin's resources directory.
      PrivacyInfo.xcprivacy         # (Required) plugin's privacy manifest file.
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
