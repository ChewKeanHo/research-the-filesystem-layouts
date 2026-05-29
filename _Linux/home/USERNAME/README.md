# `/home/[USERNAME]`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses an user's data directory. Depending on the operating
system's engineering specification, this directory can be **ENTIRELY OPTIONAL**.

This directory is accessible by the owning user, `root`, and OS administrators
(users with `wheel` permission) can access this directory.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

This directory is **ENTIRELY OPTIONAL** depending on the runtime OS usage.

Generally, you **SHOULD** place your files here.




## File Structures

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

When this directory combines with [Common](/Common) directories structure, it
houses user-only specific filesystems on top of the operating system (OS),
personalized it just for this user. The combination happens inside a `.local`
sub-directory of this directory. The commonly seen structures would be:

```
/home/
  [USERNAME]/
    .local/
      bin/
      etc/
      include/
      lib/
      sbin/
      share/
      var/
```

In the past, UNIX OSes defined a list of custom hidden user directories for easy
customization. Specifically, they are `.cache`, `.var`, `.config`, and `.fonts`.
However, for consistency and standardizations, these directories are symlinked
back to the `.local` Common sub-directories. Below are the extended list:

```
/home/
  [USERNAME]/
    .cache -> .local/var/cache
    .var -> .local/var
    .config -> .local/etc
    .fonts -> .local/share/fonts
    .local/
      bin/
      etc/
      include/
      lib/
      sbin/
      share/
      var/
```

Lastly, when an OS has an interactive user feature (e.g. graphical user
interface + desktop environment), this directory is further extended with
[User](/User) filesystems, bringing the complete list as follows:

```
/home/
  [USERNAME]/
    Desktop/
    Documents/
    Downloads/
    Pictures/
    Videos/
    Public/
    Music/
    .cache -> .local/var/cache
    .var -> .local/var
    .config -> .local/etc
    .fonts -> .local/share/fonts
    .local/
      bin/
      etc/
      include/
      lib/
      sbin/
      share/
      var/
```
