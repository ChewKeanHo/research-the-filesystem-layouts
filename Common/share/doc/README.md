# `share/doc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses non‑manual documentation files (PDF, HTML, text). These
files must be CPU‑architecture independent. For manual‑type documentation
(opened by the man program on `FreeBSD` or `Linux`‑based OSes), use `share/man/`
instead, due to the program’s directory search path.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/doc/
  trademark/
    product1/
      program.pdf
      program.txt
      ...
    product2/
      program.pdf
      program.txt
      ...
    ...
  ...

# OR

share/doc/
  product1/
    program.pdf
    program.txt
    ...
  product2/
    program.pdf
    program.txt
    ...
  ...
```
