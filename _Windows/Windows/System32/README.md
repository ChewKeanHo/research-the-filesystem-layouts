# `[DRIVE]\Windows\System32`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical programs and applications of an
operating system (OS) to function properly and minimally without any mounting
(e.g. `[DRIVE]\Program Files` is not ready or absent).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins, and `root` account to create,
update, and delete.

Generally, you **SHOULD NOT** place any files in here unless you are a Microsoft
Windows OS developer.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Microsoft Windows generally does not practice executables (e.g. `cmd.exe`) and
libraries (e.g. `kernel32.dll`) separations. Hence, all of them are placed
inside here as a single big bundle instead. They are 64-bits in nature. Hence,
the structure is something like:

```
[DRIVE]\Windows\System32\
  cmd.exe
  kernel32.dll
  ...
```
