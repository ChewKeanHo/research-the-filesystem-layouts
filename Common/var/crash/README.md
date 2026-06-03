# `var/crash`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all transient crash dumped data files. These files are
accessible by various programs, applications, and development project for an
unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD's `crash(8)` and `savecore(8)` for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  trademark/
    product/
      file1.log
      file2.log
      ...

# OR

var/crash/
  202511011500_kernel.log
  202511011530_kernel.log
  ...
  product/
    file1.log
    file2.log
    ...
```
