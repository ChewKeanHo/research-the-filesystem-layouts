# `/home/[USERNAME]/.local/share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the user-specific directory housing user-specific, user supplied,
non-critical, CPU architecture independent files (e.g. PDF files, SVG vector
image files, manual files) for extending the operating system (OS)'s
functionalities from *Complete* stage to *Personalized* stage.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




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
/home/[USERNAME]/.local/share/
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

/home/[USERNAME]/.local/share/
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
