# `share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses CPU architecture independent data files (e.g images, text,
PDFs, audio, manuals). These files are accessible by various programs,
applications, and development project for an unified repository management.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

There are 2 systems in this directory organizations:

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
