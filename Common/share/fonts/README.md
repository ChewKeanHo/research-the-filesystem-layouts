# `share/fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses font files for various programs. These files must be
CPU‑architecture independent. Depending on the OS, different font formats may or
may not be supported.

Due to font copyright and licensing sensitivities, it is **HIGHLY RECOMMENDED**
to organize fonts in a supplier‑directory‑driven manner and include the license
and copyright manuals within each supplier’s directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/fonts/
  trademark/
    product1/
      font1.tff
      LICENSE.txt
      ...
    product2/
      font2.tff
      LICENSE.txt
      ...
    ...
  ...

# OR

share/fonts/
  product1/
    font1.tff
    LICENSE.txt
    ...
  product2/
    font2.tff
    LICENSE.txt
    ...
  ...
```
