# `/dev`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system (OS) maps all the device nodes by
kernel into the filesystem for hardware-software interactions.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

Apple MacOS does not use this directory. However, it is made available for
developer power users via hidden access for BSD OS inter-compatibility purposes.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

You need to refer to the MacOS documenation for the device nodes definitions.
For examples:

* Hard disk can be repesented as:
  * `/dev/diskN` in `MacOS`.
