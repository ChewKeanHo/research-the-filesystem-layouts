# `[APPNAME].app/[APPNAME]Clip`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's integrated Apple App Clips "bundle". It is a
lightweight version of the app offering some functionalities when and where need
it for new users trying out the full app.

App Clips "bundle" is an extension from the full app where assets and resources
files are completely reusable.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Depending on XCode version, App Clips can be directly integerated via the main
app's single entry point source code.
