# `/var/cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all production cache files from one or more services.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `cache`** as it represent the entire caching
directory.

The file extension can be anything.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/cache/
  trademark/
    product/
      data.save
      profile1.jpg
      transient.json
      ...

OR

/var/cache/
  product/
    data.save
    profile1.jpg
    transient.json
    ...
```
