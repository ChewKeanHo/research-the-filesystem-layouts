# `var/preserve`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient preserved data files for historical tracing.
They are stored for historical reference and tracing. For backup files, use
`var/backups/` instead.




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
