# `[PLUGINNAME].bundle/Contents`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses a plugin bundle's contents. This plugin complies to MacOS
bundle filesystem structure.

If you are developing using XCode, then you may structure your content
accordingly.

Otherwise, whether the bundle is procured from Apple AppStore or elswehere, one
should **DEFINITELY MUST NOT** place or modify any files and folders inside the
bundle for avoiding any breakage (e.g. signed signature).
