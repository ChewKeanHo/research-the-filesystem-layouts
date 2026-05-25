# `/root/.config`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is a functional directory used for housing configuration files from
user-specific programs and applications. Most UNIX and UNIX-like OSes create
this directory as it is. Otherwise, modern OSes symlinked it to the
`/root/.local/etc` directory, a `.local` common directory for consistency with
the filesystem hierarchy standards.

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

To symlink this directory to `/root/.local/etc` manually, simply execute the
following command:

```
# cd "/root"
$ mkdir -p "./.local/etc"
$ if [ -d "./.config" ]; then do mv "./.config/*" "./.local/etc/."; done
$ rm -rf "./.config" &> /dev/null
$ sync .
$ ln -s "./.config" "./.local/etc"
```
