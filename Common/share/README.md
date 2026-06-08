# `share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent files (e.g. PDF, images,
text, audios, manuals) that are portable in nature and usable across various CPU
hardware. Hence the name `share/` is provisioned. Unlike other directories, this
directory has known functionally named first level sub-directories like
`share/doc/` is for PDF, text, HTML documents, `share/locale` is for
internationalization translation data files, etc.

These sub-directories listed are abstracted and known to exist across all
deployment. While it is not a rule to comply all of them, it is better to use
them for maximizing compatibility and portability. When a functional directory
is unavailable (e.g. `share/music`), one can defines the functional directory
after researching all others OSes’ implementation. If any of them already
defined one, when sensible, use that instead.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

There are 2 known patterns in this directory organizations:

* functional directories (e.g. `fonts`, `doc`, `man`).
* non-functional directories.

Before designating where to place the files, one **MUST** check the functional
directory's availability before implementing the latter pattern.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern for both of them. This can significantly reduces the
naming collision for common names. Deploy them accordingly for all the
directory organizations above.

Here are the examples:

```
share/
  doc/
    trademark/
      product1/
        program1.pdf
        program1.txt
        ...
      product2/
        program2.pdf
        program2.txt
        ...
      ...
    ...
  man/
    trademark/
      product1/
        man1/
          amd64
          aarch64
          ...
        man2/
          amd64
          aarch64
          ...
        ...
      product2/
        man1/
          amd64
          aarch64
          ...
        man2/
          amd64
          aarch64
          ...
        ...
      ...
    ...
  fonts/
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
  ...
  trademark/                      # when functional directory is unavailable
    product3/
      resources/
        background.svg
        background.webm
        ...
      licenses/
        LICENSE.pdf
        LICENSE.txt
        LICENSE.html
        ...
      ...

# OR

share/
  doc/
    product1/
      program1.pdf
      program1.txt
      ...
    product2/
      program2.pdf
      program2.txt
      ...
    ...
  man/
    product1/
      man1/
        amd64
        aarch64
        ...
      man2/
        amd64
        aarch64
        ...
      ...
    product2/
      man1/
        amd64
        aarch64
        ...
      man2/
        amd64
        aarch64
        ...
      ...
    ...
  fonts/
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
  product3/                       # when functional directory is unavailable
    resources/
      background.svg
      background.webm
      ...
    licenses/
      LICENSE.pdf
      LICENSE.txt
      LICENSE.html
      ...
  ...
```
