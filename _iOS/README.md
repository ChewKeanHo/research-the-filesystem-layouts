# `[APPNAME].app`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This section covers all Apple `iOS` app's sandbox filesystem. Installer creates
a number of container directories for the app lives inside the sandbox
directory.

An app is **generally prohibited** from accessing or creating files outside its
container directories.

There are 3 types of containers per sandbox:

* **Bundle Container** - holds the [Apple iOS App bundle](/_iOS.app).
* **Data Container** - holds the app's data files.
  * **`Documents`** - holds documents data files.
  * **`Library`** - holds library data files.
  * **`Temp`** - holds short-lived temporary data files.
* **iCloud Container** - holds the app's iCloud connected data files.
