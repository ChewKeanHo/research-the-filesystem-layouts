# `/usr/share`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing system-wide, operating system (OS)
distributor supplied, non-critical, CPU architecture independent data files
(e.g images, text, PDFs, audio, manuals) of an OS to function properly. This
means it can operate in `Multi-User` mode in BSD realm or `Full Mode` in Linux
realm.

The goal is to extend the OS' functionalities all the way to its OS
distributor's supplied packages. All payloads, filepaths, configurations, data,
etc. are strictly registered by the OS distributor for achieving uniformity
and consistency across ALL hardware (fleet management).

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way. Use `/usr/local/share` or
`${HOME}/[USERNAME]/.local/share` instead.

This directory **MUST NOT** have any sub-directory.




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
/usr/share/
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

/usr/share/
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
