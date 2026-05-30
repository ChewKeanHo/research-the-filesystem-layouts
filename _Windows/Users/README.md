# `[DRIVE]\Users`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all user level data directory. The first-level
sub-directory name is usually mapped to:

* an user's username or user identity; AND
* a global `Public` identity accessible by everyone.

The control is defined by Windows Account Management therefore it is not a
compulsory rule for the strict username matching.

The goal is to extend the OS' functionalities from *Complete* stage to
*Personalized* stage.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD NOT** place any files in here unless you are a software
developer. Installed programs are housed in the `[DRIVE]\Users\[USERNAME]`
directory instead.

This directory is accessible via the the following environment variables:

* `%PROFILESFOLDER%`




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each downstream directory in details.
