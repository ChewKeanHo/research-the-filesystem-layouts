# `[DRIVE]\Windows`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system (OS)'s distributor supplied
non-critical programs, applications, libraries, configurations, boot, and files.
It is read-only for preventing unwanted temperment.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like facilitating
`[DRIVE]/Program Files` OS System Resources directories for functionalities
extension, performing self-rescue, or straight up operational in resources
constraint environment. The OS achieves *Minimum & Critical* stage when the
initialization is successful.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Generally, you **SHOULD NOT** place any files in here unless you are a Microsoft
Windows OS developer.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

This directory is accessible via the the following environment variables:

* `%WINDIR%`
* `%SYSTEMROOT%`




## Primary Objectives

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each downstream directory in details. Once done, head over to
[`Program Files`](/_Windows/Program%20Files) directory which is the next
system-level layer for functionalities expansions.
