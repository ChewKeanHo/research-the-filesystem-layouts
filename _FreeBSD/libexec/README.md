# `/libexec`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This is the base directory for housing critical, non-commandable programs and
applications of an operating system (OS) to function properly and minimally
without any mounting (e.g. `/usr` is not mounted or absent). This means it can
operate in `Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform critical tasks like mounting `/usr` UNIX System
Resources directory for OS capabilities extension, performing self-rescue, or
straight up being operational in this resources constraint environment such as
but not limited to OpenWRT embedded router.

All programs and applications here are **NOT AVAILABLE** as callable commands.
To execute, the full filepath is used instead.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and `root`
account to create, update, and delete.

In some `Linux`-based OSes like Oracle's Solaris (first to transform back in
2012) and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is
always being mounted and hardware are no longer observing performance compromise
between `/` and `/usr` layers, `/usr/libexec` directory is being symbolic linked
to `/libexec` instead; unifying both directories. This reduces the separation
complexities for package managements and distributions as all packages only
needs to target `/usr/libexec` directory.

In FreeBSD, this directory is still maintaining its verbatim separated roles and
responsibilites from `/usr/libexec` directory.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.

Generally, you **SHOULD NOT** place anything here **UNLESS** you are the OS
distributor. This is to avoid any conflict with the upstream's registries that
will break the OS updates or upgardes in any way. Use `/usr/local/libexec` or
`${HOME}/[USERNAME]/.local/libexec` instead. In the case of `/libexec` being
symbolically linked from `/usr/libexec`, you **MUST** place the content in
`/usr/libexec` instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

All POSIX compliant registered programs based on IEEE POSIX1.0 list
(refer: https://pubs.opengroup.org/onlinepubs/9799919799/idx/utilities.html).

Among the known ones are:

```
[        - program to test a condition (used in shell scripting).
cat      - program to concatenate files to standard output.
chgrp    - program to change file group ownership.
chmod    - program to change file access permissions.
chown    - program to change file ownership and group.
cp       - program to copy files and directories utility.
date     - program to print and set datetime.
dd       - program to duplicate raw input/output.
df       - program to report filesystem and disk space capacity.
dmesg    - program to print or control kernel message buffers.
echo     - program to display content.
false    - program to do nothing or unnecessfully.
hostname - program to show OS's hostname.
kill     - program to kill a process.
ln       - program to make link in filesystem.
login    - program to login.
ls       - program to list item in filesystem.
mkdir    - program to make directory.
mknod    - program to make block or character special files.
more     - program to page through text.
mount    - program to mount a filesystem.
mv       - program to move things in filesystem.
ps       - program to report process status.
pwd      - program to report current directory location.
rm       - program to remove item in filesystem.
rmdir    - program to remove empty directory in filesystem.
sed      - program to stream and edit files in filesystem.
sh       - program to execute POSIX compatible shell.
stty     - program to configure terminal settings.
su       - program to change runtime user ID.
sync     - program to flush buffers in filesystem.
test     - program to test a condition.
true     - program to do nothing successfully.
umount   - program to unmount a filesystem.
uname    - program to report OS system information.
```

Optional programs (for more robust critical functionalities) are:

```
tar      - program to archive a directory.
cpio     - program to archive a directory.
gzip     - program by GNU for compression.
gunzip   - program by GNU for de-compression.
zcat     - program by GNU for de-compression.
netstat  - program to report network statistics.
ping     - program to perform ICMP network testing.
```
