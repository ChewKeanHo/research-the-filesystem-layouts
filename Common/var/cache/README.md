# `var/cache`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient cache data files for performance enhancement.
Programs must not depend solely on these files; they **MUST HAVE** algorithms to
create, update, and delete them.




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
