# `var/db`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all transient database and datastore files. These files
are accessible by various programs, applications, and development project for an
unified repository management.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.




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
