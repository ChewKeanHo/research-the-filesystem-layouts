# `/etc`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s critical and distributor
supplied configuration files to function properly and minimally without any
mounting (e.g. `/usr` is not mounted or absent). This means it can operate in
`Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimum possible configuration files for the OS to
initialize as intended achieving basic functionalities. This allows the OS to
perform critical tasks like mounting `/usr` UNIX System Resources directory for
functionalities extension, performing self-rescue, or straight up operational in
resources constraint environment such as but not limited to OpenWRT embedded
router.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Generally, you **SHOULD ONLY** place or modify system-level configuration files
that are very critical to the operating systems excluding bootloader artifacts
(as they are housed inside `/boot`, `/boot/efi`, or `/efi` respectively
instead). However, bootloader artifacts' generator is allowed here as it is part
of the operating system maintenance tool.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy also reduces the configuration
complexities and making maintainability easier by just updating 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples:

```
/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
