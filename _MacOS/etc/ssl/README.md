# `/etc/ssl`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This base directory houses all operating system (OS)'s OpenSSL's configuration
files. It has critical files and the certificate archives. This means it can
operate in `Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

For FreeBSD, this directory houses the following files:

```
/etc/ssl/
  cert.pem        # System trust store in bundle form.
  openssl.cnf     # OpenSSL configuration file.
```

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD ONLY** modify the configuration files that are very
critical to the OS after referring to the FreeBSD's OpenSSL specification. You
**SHOULD NOT** place any files here.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

Refer `certctl(8)` and `openssl` manuals for the specifications and
file directory structures.
