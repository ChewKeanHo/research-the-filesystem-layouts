# `var/log`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses transient log files for forensic analysis. While generally
text‑based, log files tend to grow exponentially large. It is therefore best to
use a log rotation program to split logs into smaller, meaningful fragments.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `log`** as it represent the entire logging
service.

The file extension can either be `.txt` or `.log`.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
var/log/
  trademark/
    product/
      20251201_info.log
      20251202_info.log
      ...
    ...
  ...

OR

var/log/
  product/
    20251201_info.log
    20251202_info.log
    ...
  ...
```
