# `share/games`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses game engine resource files (models, engine configurations,
manifest files) for gaming programs. These files **MUST BE** CPU‑architecture
independent.

For user‑specific game data (saved games, screenshots), use `var/games/`
instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
share/games/
  trademark/
    product/
      dict.dat
      i18n.toml
      data.bin
      ...
    ...
  ...

OR

share/games/
  product/
    dict.dat
    i18n.toml
    data.bin
    ...
  ...
```
