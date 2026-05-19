# `[APPNAME].app/Contents`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an app's contents. This app complies to MacOS bundle
filesystem structure.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding breakage (e.g. signed signature).
