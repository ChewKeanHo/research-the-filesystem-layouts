# `/mnt`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing temporary mounted removable media device such
as but not limited to CD, floppy disks, USB storage devices, external disks,
decrypted partitions, or volume managed partitions. This is used by sysadmins
and root account users only to debug a mountable device, volume files, or
device partition.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

For production deployment or permanent mounting, use `/media` base directory
instead.
