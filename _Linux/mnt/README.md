# `/mnt`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing a single removable media temporarily such
as but not limited to CD, floppy disks, USB storage devices, external disks,
decrypted partitions, and volume group managed partitions.

The purpose is to cater a fixed location for `root` account and operating
system (OS)'s to debug a hardware device or a partition's filesystem problem.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.

For production deployment or permanent mounting, use `/media` base directory
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `automount(8)` and `bsdisks(8)` manuals for specifications.
