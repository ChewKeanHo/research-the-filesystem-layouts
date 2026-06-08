# `tmp`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses temporary files and directories for any program to use
during an operation (e.g., unpacking a compressed archive). Due to the high
traffic, it is **HIGHLY RECOMMENDED** to clean up (delete) before and after use
to prevent data corruption and unwanted storage consumption.

Depending on the deployment, this directory's lifetime may be temporary or
permanent. On most systems it is cleared on reboot. Some, like `/var/tmp` on
`FreeBSD` and `Linux`-based OSes, have a permanent lifetime to store crash or
reboot logs.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
tmp/
  trademark/
    product/
      ...
    ...
  ...

OR

tmp/
  product/
    ...
  ...
```
