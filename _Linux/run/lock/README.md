# `/run/lock`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all operating system's (OS) serial devices' lock files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In some Linux-based OSes like Red Hat Linux, SystemD, and UAPI, this directory
is **REPLACING** `/var/lock` for reducing total numbers of used `tmpfs`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `lock`** as it represent the entire data
directory.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/run/lock/
  trademark/
    product/
      service1.lock
      service2.lock
      data1.lock
      profile1.lock
      ...

# OR

/run/lock/
  product/
    service1.lock
    service2.lock
    data1.lock
    profile1.lock
    ...
```
