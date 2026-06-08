# `var/backups`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient backup data files.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **plural `backups`** as it represent the entire backup
directory.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/backups/
  trademark/
    product/
      data.save
      profile1.jpg
      transient.json
      ...
    ...
  ...

OR

var/backups/
  product/
    data.save
    profile1.jpg
    transient.json
    ...
  ...
```
