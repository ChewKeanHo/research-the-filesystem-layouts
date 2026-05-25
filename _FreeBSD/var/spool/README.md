# `/var/spool`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) spooling tasks' data files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on usage in the runtime OS.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




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
/var/spool/output/
  trademark/
    product/
      file1
      file2
      ...
  ...

OR

/var/spool/output/
  product/
    file1
    file2
    ...
  ...
```
