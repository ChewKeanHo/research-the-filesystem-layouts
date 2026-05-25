# `/root/.fonts`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing user-only and user-specific font
files. Most UNIX and UNIX-like operating system (OS)s create this directory as
it is. Otherwise, modern OSes symlinked it to the `/root/.local/share/fonts`
directory, a `.local` common directory for consistency with the filesystem
hierarchy standards.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

**Only `root` and administrators (users with `wheel` permission) can access the
directory**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

Generally, unless absolute necessary, you **SHOULD NOT** place anything here
**UNLESS** you are the OS distributor. This is to avoid any conflict with the
upstream's registries that will break the OS in any way. Use `/home/[USERNAME]`
instead.

To symlink this directory to `/root/.local/share/fonts` manually, simply execute
the following command:

```
# cd "/root"
$ mkdir -p "./.local/share/fonts"
$ if [ -d "./.fonts" ]; then do mv "./.fonts/*" "./.local/share/fonts"; done
$ rm -rf "./.fonts" &> /dev/null
$ sync .
$ ln -s "./.fonts" "./.local/share/fonts"
```
