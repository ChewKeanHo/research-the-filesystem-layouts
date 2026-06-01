# `/spool`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing all runtime spooling data files of an
operating system (OS) to function properly. The goal is to provision spooling
functionalities like paper printing for the OS.

This directory is marked **AS COMPULSORY TO EXIST** by Linux's Filesystems
Standards (https://specifications.freedesktop.org/fhs/latest/varRequirements.html).
However, in practice, this directory is **OPTIONAL** depending on the runtime
OS uses and specifications.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

You **DEFINITELY MUST NOT** place anything here. Let the OS controls it
entirely.

In FreeBSD, this is unused.

In Linux-based OSes, many OSes are migrating the runtime `tmpfs` into this
directory mainly for reducing the total use of `tmpfs` counts. For supporting
backward compatibility, some OSes is symlinking this directory to `/var/spool`
directory.

In MacOS, this is unused.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `spool`** as it represent the entire mail
directory.

The file extension can be anything and nothing. The first sub-directory layer is
the task name. Then, it is a practice to house the configuration files using
`trademark` and `product` as filename. This directory structure is special as it
depends on the mailing services the OS is using.

Here are the examples:

```
/spool/
  output/
    trademark/
      product/
        file1
        file2
        ...
    ...

OR

/spool/
  output/
    product/
      file1
      file2
      ...
  ...
```
