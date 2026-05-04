# `AppName.app` (App Bundle)

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an application bundle container in Apple iOS bundle
specification. This is used to operate a procured application from App Store.

One **CANNOT WRITE** to this directory and the directory is signed at
installation time for tempering prevention. If one successfully written into it,
the signature will change and the app will not load on launch. However, between
applications can gain read-only access on each other's resources.

The contents are not back up by iTunes or iCloud. However, iTunes does perform
an initial sync of any apps purchased from the App Store.
