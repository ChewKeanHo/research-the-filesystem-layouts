# `/Users/[USERNAME]/Library/Frameworks`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses all library framework bundles installed by a specific user
without needing an administrator (users with `wheel` permission) privilege. App
procured via a digital store can be placed here automatically.

Users **SHOULD BE** allowed for manual modifications. Otherwise, they will start
being sliently rebelious cracking the operating system (OS) which is an
undesirable move.

For security, an OS can implement content cryptographic signing and
distributor's notarizations like how Apple Developer Program works.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission).

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## OS Deployment

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory was first spotted in the following OSes:

1. Apple's `MacOS`.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
Library/Frameworks/
  trademark/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...
    ...
  ...

# OR

Library/Frameworks/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
  ...
```
