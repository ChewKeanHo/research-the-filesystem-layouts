# `/dev`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system (OS) maps all the device nodes by
kernel into the filesystem for hardware-software interactions.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

This directory is part of the `local domain`.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the MacOS documenation for the device nodes definitions.
For examples:

* ATA Hard disk (SATA) storage device can be repesented as:
    * `/dev/diskN` in `MacOS`.
* Floppy Disk storage device can be repesented as:
    * unsupported.
* NVME storage device can be repesented as:
    * `/dev/diskN` in `MacOS`.
* Null device can be represented as:
    * `/dev/null` in `MacOS`.
* SecureDigital (SD) or Multimedia Card (MMC) storage devices can be repesented
  as:
    * `/dev/diskN` in `MacOS`.
* Optical compat disc (CD) storage device can be repesented as:
    * `/dev/diskN` in `MacOS`.
    * `/dev/cdrom` as symlink in `MacOS`.
* SCSI Hard disk storage device can be repesented as:
    * `/dev/diskN` in `MacOS`.
* Strong randomness devices can be represented as:
    * `/dev/random` (high quality) in `MacOS`.
    * `/dev/urandom` (regardless of entropy) in `MacOS`.
* Tape storage device can be repesented as:
    * unsupported.
* USB serial device can be represented as:
    * `/dev/cu.usbserial-NNNN` in `MacOS`; OR
    * `/dev/tty.usbserial-NNNN` in `MacOS`.
* USB storage device can be represented as:
    * `/dev/diskN` in `MacOS`.
