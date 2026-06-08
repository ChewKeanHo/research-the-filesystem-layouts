# `libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non‑command‑able programs and applications. They are
explicitly and intentionally not mapped to `$PATH`. Users must use the full
filepath (e.g., `/bin/date` instead of `date`) to execute them.

This directory is intentionally designed to house internal or subroutine
executable called by the main programs and applications elsewhere. The caller
can be anything like program, application, init server, a time scheduler, etc.
This is the sole reason why they are not mapped into the commands list.

Unlike its counterparts like `bin/` or `sbin/` directories, the use of
sub-directory is allowed since they are not mapped into the commands list.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
libexec/
  trademark/
    product/
      process-day.sh
      process-week.sh
      ...
    ...
  ...

# OR

libexec/
  product/
    process-day.sh
    process-week.sh
    ...
  ...
```
