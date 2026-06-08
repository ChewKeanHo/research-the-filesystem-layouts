# `var/db`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient database files critical for operations. This
directory **MUST BE** targeted for routine backup to reduce the risk of data
loss.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/db/
  trademark/
    product/
      node1
      node2
      file1.data
      file2.data
      ...
    ...
  ...

# OR

var/db/
  product/
    node1
    node2
    file1.data
    file2.data
    ...
  ...
```
