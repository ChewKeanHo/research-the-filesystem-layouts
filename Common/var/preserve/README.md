# `var/preserve`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all transient unused and presented for historical reasons
data files. These files are accessible by various programs, applications, and
development project for an unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/preserve/
  trademark/
    product/
      node1
      node2
      file1.data
      file2.data
      ...
  ...

# OR

var/preserve/
  product/
    node1
    node2
    file1.data
    file2.data
    ...
  ...
```
