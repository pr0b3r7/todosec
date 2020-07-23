---
description: Check various logs in RHEL5
---

# Linux Logs

Reference: https://access.redhat.com/documentation/en-us/red\_hat\_enterprise\_linux/5/html/deployment\_guide/ch-logfiles

`cat /etc/syslog.conf`

## Contents of syslog.conf

" \# Log all kernel messages to the console. Logging much else clutters up the screen.

`kern.*                                                 /dev/console`

### Log anything \(except mail\) of level info or higher.

Don't log private authentication messages!

`*.info;mail.none;authpriv.none;cron.none /var/log/messages`

## The authpriv file has restricted access.

`authpriv.* /var/log/secure`

## Log all the mail messages in one place.

`mail.* -/var/log/maillog`

## Log cron stuff

`cron.* /var/log/cron`

## Everybody gets emergency messages

_`.emerg`_ 

## Save news errors of level crit and higher in a special file.

`uucp,news.crit /var/log/spooler`

## Save boot messages also to boot.log

`local7.* /var/log/boot.log`

## Log all messages to a remote logging server:

`.   @server.domain.com"`

