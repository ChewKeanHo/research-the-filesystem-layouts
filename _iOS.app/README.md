# `[APPNAME].app`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is an Apple's `iOS` app bundle filesystem structure. A single app is a
project of its own. For `iOS`, this is clean and slim directory housing
everything required at the root directory. This is used to operate a procured
application from App Store.

All iOS apps can only have read permission between each other's resources. The
contents are not back up by iTunes or iCloud. However, iTunes does perform an
initial sync of any apps purchased from the App Store.

For iOS app, there is no `Resources/` directory. Hence, this directory also
houses an app's resources files used by the app's single main entry point
executable.

Modern iOS development involves multi-interfacing targets such as but no limited
to:

* `watchOS`  - for Apple Watch devices.
* `AppClips` - for seamless iOS app's graphical user experience.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Below is
a currently updated structure:

Each app **MUST** have the `.app` file extension for identification.

```
[APPNAME].app
  [APPNAME]                       # (Required) app's executable entry point.
  [APPNAME].icns                  # (Required) app's ".icn" icon file.
  [APPNAME]Clip/                  # app's appClips bundle.
    ...
  [APPNAME] Watch App/            # app's associated watchOS app
    ContentView                   # watchOS's single main control Swift source code.
    Assets                        # watchOS's graphical assets.
    Frameworks/
      [FRAMEWORKNAME].framework/  # watchOS's externally added frameworks.
      ...
    PlugIns/
      [PLUGIN].bundle/            # watchOS's externally added plugin bundles.
      ...
    ...
  embedded.mobileprovision        # (Required) app's provisioning profile.
  Frameworks/
    [FRAMEWORKNAME].framework/    # app's externally added frameworks.
    ...
  Info.plist                      # (Required) app's metadata.
  PlugIns/
    [PLUGIN].bundle/              # app's externally added plugin bundles.
    ...
  PrivacyInfo.xcprivacy           # (Required) app's privacy manifest file.
  Sounds/                         # resources located at root directory.
    intro.wav
    ...
  Images/                         # resources located at root directory.
    banner.avif
    ...
  en.lproj/                       # organized localized resources
    InfoPlist.strings
    Localizable.strings
    ...
    Images/                       # resources specific to this localization
      logo.avif
      ...
  jp.lproj/                       # organized localized resources
    InfoPlist.strings
    Localizable.strings
    ...
    Images/                       # resources specific to this localization
      logo.avif
      ...
```
