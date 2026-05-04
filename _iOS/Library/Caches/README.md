# `Library/Caches`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses re-creatable and performance-improving files. App is
solely managing the content of this directory for adding, updating, and deleting
as needed.

All content in this directory should be placed in a custom sub-directory whose
name is that of your app’s bundle identifier or your company.

OS can delete this directory when it is very low on disk space when the app is
not running.

Backup restoration is not necessarily means this directory can be erased.

The content are not backed up by iTunes and iCloud.
