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

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the OS distributor's documentations for the device nodes
definitions. For examples:

* ATA Hard disk (SATA) storage device can be repesented as:
    * `/dev/sdN` in `Linux`.
* Floppy Disk storage device can be repesented as:
    * `/dev/fdN` in `Linux`.
* NVME storage device can be repesented as:
    * `/dev/nvmeNnM` in `Linux`.
* Null device can be represented as:
    * `/dev/null` in `Linux`.
* SecureDigital (SD) or Multimedia Card (MMC) storage devices can be repesented
  as:
    * `/dev/mmcblkN` in `Linux`.
* Optical compat disc (CD) storage device can be repesented as:
    * `/dev/srN` in `Linux`.
* SCSI Hard disk storage device can be repesented as:
    * `/dev/sdN` in `Linux`.
* Strong randomness devices can be represented as:
    * `/dev/random` (high quality), `/dev/urandom` (regardless of entropy) in `Linux`.
* Tape storage device can be repesented as:
    * `/dev/stN` in `Linux`.
* USB serial device can be represented as:
    * `/dev/ttyUSBN` in `Linux`.
* USB storage device can be represented as:
    * `/dev/sdN` in `Linux`.
