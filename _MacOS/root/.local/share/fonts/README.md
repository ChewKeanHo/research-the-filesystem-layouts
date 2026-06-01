# `/root/.local/share/fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the `root` account's directory housing user-specific, user supplied,
non-critical, CPU architecture independent font files for extending the
operating system (OS)'s functionalities from *Complete* stage to *Personalized*
stage.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ONLY** accessible `root` and OS administrators (users with
`wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD** place your files here. All of them are only available
specifically for you.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/root/.local/share/fonts/
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

/root/.local/share/fonts/
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
