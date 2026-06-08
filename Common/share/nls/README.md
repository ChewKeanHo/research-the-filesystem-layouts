# `share/nls`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses national language support data files. These files
**MUST BE** CPU‑architecture independent. This directory is specific to
`UNIX`‑based OSes (`FreeBSD`, `Linux`-based OSes). On other systems it is left
blank.

This directory is specific to `UNIX`-based OSes like `FreeBSD` and `Linux`-based
OSes. Otherwise, it is always left blank.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/nls/
  trademark/
    product/
      template1.mk
      template2.mk
      ...
    ...
  ...

OR

share/nls/
  product/
    template1.mk
    template2.mk
    ...
  ...
```
