# `var/cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all transient cache data files. These files are accessible
by various programs, applications, and development project for an unified
repository management.

It is always recommended to clean up the cached files algorithmically to avoid
any cache-poisoning corruption or hogging unwanted storage spaces.




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
var/cache/
  trademark/
    product/
      data.save
      profile1.jpg
      transient.json
      ...
    ...
  ...

OR

var/cache/
  product/
    data.save
    profile1.jpg
    transient.json
    ...
  ...
```
