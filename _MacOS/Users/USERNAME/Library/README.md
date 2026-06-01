# `/Users/[USERNAME]/Library`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses user-specific configuration files (e.g. app libraries or
internal system files).

App is allowed to create additional directory here. Any app **SHOULD NOT**
assume any file or directory and always perform safe query before use.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is part of the `local domain`.

Depending on content, you **MAY** be able to place or modify any files and
folders manually. Otherwise, you **DEFINITELY MUST NOT** do so and let the
installed apps handle it.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The first-level directory name is recommended to be functional (e.g. `Fonts`,
`Frameworks`, `Preferences`). Then, it is a practice to house the files using
`trademark` and `product` sub-directories pattern. This can significantly
reduces the naming collision for common names.

Here are the examples:

```
/Users/[USERNAME]/Library/
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
    frame1.framework
    plugin1.bundle
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

/Users/[USERNAME]/Library/
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
    frame1.framework
    plugin1.bundle
    ...
  Preferences/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...
```
