
First5 Logwatch Role
==============

[![Build Status](https://travis-ci.org/Blue-Bag/ansible-first5-logwatch.svg?branch=main)](https://travis-ci.org/Blue-Bag/ansible-first5-logwatch)


Install and configure Logwatch.

Role Variables
--------------------
These are commented in the defaults file.

The config is written to `/etc/logwatch/conf/logwatch.conf`. Do not move it back to
`/usr/share/logwatch/default.conf/`: that file belongs to the package and is replaced on every
logwatch upgrade.

The role also writes `/etc/logwatch/conf/services/iptables.conf` so the "iptables firewall" section
reads `kern.log`. The stock service reads `/var/log/messages`, which Debian 12 and later no longer
write.

Usage
---------



# Running logwatch manually
logwatch --detail Med --mailto info@example.com  --range yesterday

logwatch --detail Medium --mailto info@example.com --service All --range today



License
-------
BSD

Author Information
------------------
George Boobyer - Blue-Bag Ltd
