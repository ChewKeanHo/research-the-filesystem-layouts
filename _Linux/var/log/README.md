# `/var/log`

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

This directory houses log data files. It is recommended to rotate the log files
before use (e.g. by datetime or id number increment) to avoid post-use blaming
or data loss.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

All files here are available to all users to read but **ONLY** available to
specific user with permission, all sysadmins (user in `wheel` group), and root
account to create, update, and delete.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

In Apple `MacOS`, this directory is facilitated mainly for supporting BSD
inter-compatibilities purposes only. `MacOS` does not not really use and depend
on it. Also this directory is part of the `local domain`.




## Naming Convention

[![banner](/.internals/trademarks/banner_1200x100.svg)](#)

The naming convention is **singular `log`** as it represent the entire logging
service.

The file extension can either be `.txt` or `.log`.

It is a practice to house the files using `trademark` and `product`
sub-directories pattern. This can significantly reduces the naming collision for
common names.

Here are the examples:

```
/var/log/
  trademark/
    product/
      20251201_info.log
      20251202_info.log
      ...

OR

/var/log/
  product/
    20251201_info.log
    20251202_info.log
    ...
```

Known log files are:

```
/var/log/
  Xorg.0.log            # `Xserver(1)` log, if `X(7)` is installed rotates to
                        # `Xorg.0.log.old`
  aculog                # serial line access log; see `cu(1)`.
  auth.log              # system authentication log.
  bsdinstall_log        # system installation log.
  cron                  # scheduled task log; see `cron(8)`.
  cups/                 # logs for `cups(1)`.
    ...
  daemon.log            # default log for system daemons.
  devd.log              # default log for device state change daemon.
  dmesg.today           # system  message  buffer log, rotates to
                          dmesg.yesterday.
  debug.log             # undiscarded debug syslog messages.
  lpd-errs              # logs for the line printer spooler daemon. Refer
                        # `lpd(8)`.
  maillog               # `sendmail(8)` log, rotates and compresses to
                        # maillog.0.bz2.
  messages              # general system log; see `syslogd(8)`.
  mount.today           # currently loaded `fstab(5)`, rotates to
                        # mount.yesterday.
  pf.today              # packet filter firewall log;  see `pf(4)`.
  pflog                 # saved packets caught by `pflogd(8)`.
  ppp.log               # see `ppp(8)`.
  security              # transcript of events marked with the security flag.
  setuid.today          # listing of executable files which run with elevated
                          permissions, rotates to setuid.yesterday.
  userlog               # logs changes in users or groups.
  utx.lastlogin         # last login log; see `getutxent(3)`.
  utx.log               # login/logout log; see `getutxent(3)`.
```
