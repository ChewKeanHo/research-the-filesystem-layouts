# `share/locale`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses internationalization resource files. These files
**MUST BE** CPU‑architecture independent. The first sub-directory's name is the
language ID (`[ISO639]{-[ISO15924]}{-[ISO3166]}`). The designer may structure
the contents arbitrarily.

File formats are at the supplier's discretion; common formats are machine object
(`.mo`), TOML (`.toml`), or YAML (`.yml`), but the context remains the same.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer FreeBSD's `setlocale(3)` manual for specifications.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/locale/[LAND_ID]/
  trademark/
    product/
      encryption.mo
      encryption.toml
      encryption.yml
      sign.mo
      sign.toml
      sign.yml
      ...
    ...
  ...

OR

share/locale/[LAND_ID]/
  product/
    encryption.mo
    encryption.toml
    encryption.yml
    sign.mo
    sign.toml
    sign.yml
    ...
  ...
```
