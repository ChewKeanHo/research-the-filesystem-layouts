# `Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all packaged library bundles installed by the owning user
without requiring administrator privileges (e.g. a user with `wheel` privilege
on `UNIX`-based OSes). It was first introduced by Apple’s `MacOS`, where
user‑specific library bundles are placed here.

For security, an operating system may implement content cryptographic signing
and distributor notarization.




## OS Deployment

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory was first spotted in the following OSes:

1. Apple's `MacOS`.
2. Microsoft `Windows` (It is called `AppData/Roaming` instead).




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The first-level directory name is recommended to be functional (e.g. `Fonts`,
`Frameworks`, `Preferences`). Then, it is a practice to house the files using
`trademark` and `product` sub-directories pattern. This can significantly
reduces the naming collision for common names.

Here are the examples:

```
Library/
  Fonts/
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
  Frameworks/
    trademark/
      product/
        lib1.so
        lib1_freebsd-amd64.so
        kernel8.ko
        kernel8_freebsd-amd64.ko
        ...
  Preferences/
    trademark/
      product/
        settings.d/
          setting1.conf
          setting2.conf
          ...
        ...
      ...
    ...
  ...

# OR

Library/
  Fonts/
    product1/
      font1.tff
      LICENSE.txt
      ...
    product2/
      font2.tff
      LICENSE.txt
      ...
    ...
  Frameworks/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...
  Preferences/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...
```
