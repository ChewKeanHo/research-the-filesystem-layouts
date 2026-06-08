# `var/account`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient user identity and access management data files.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/account/
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

var/account/
  product/
    node1
    node2
    file1.data
    file2.data
    ...
  ...
```
