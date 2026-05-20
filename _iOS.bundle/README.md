# `[PLUGINNAME].bundle`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is an Apple's `iOS` plugin bundle filesystem structure. A single plugin
is a project of its own. Unlike app bundles, plugin **DOES NOT** have a single
main entry executable to maintain.

For iOS app, there is no `Resources/` directory. Hence, this directory also
houses an app's resources files used by the app's single main entry point
executable.

If you are developing using XCode, then you may structure your content
accordingly.

Since `iOS` is **DISALLOWED AND PROHIBITED** to create a framework bundle on
production, plugin bundle is only used in XCode development as app imported
module.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is entirely upto the Apple's XCode to structure this directory. Below is the
`iOS` directory structure.

Each app **MUST** have the `.bundle` or `.plugin` file extension for
identification.

```
[PLUGINNAME].bundle
[PLUGINNAME].bundle
  [PLUGINNAME]                       # some executable.
  [PLUGINNAME].icns                  # plugin's ".icn" icon file.
  embedded.mobileprovision        # (Required) plugin's provisioning profile.
  Frameworks/
    [FRAMEWORKNAME].framework/    # plugin's externally added frameworks.
    ...
  Info.plist                      # (Required) plugin's metadata.
  PlugIns/
    [PLUGIN].bundle/              # plugin's externally added plugin bundles.
    ...
  PrivacyInfo.xcprivacy           # (Required) plugin's privacy manifest file.
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
