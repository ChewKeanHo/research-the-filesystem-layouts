# `/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non-user files (e.g. app libraries or internal system
files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

For `iOS`, apps are **DISALLOWED AND PROHIBITED** to create a framework. Hence,
the `/Library/Frameworks` is definitely unavailable.

You **DEFINITELY MUST NOT** place or modify any files and folders manually here
for avoiding breakage. Let the installed apps handle it.

The content are backed up by iTunes and iCloud.
