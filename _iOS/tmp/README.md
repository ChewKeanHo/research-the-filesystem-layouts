# `/tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all temporary files that do not need to persist between
launches of an app. App should remove the files when they are no longer needed.

System may purge this directory when app is not running.

The contents are not backed up by iTunes and iCloud.
