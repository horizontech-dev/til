---
date: 2020-07-17T08:22:51-07:00
title: debug-systemd-issues-in-buster
tags: OS
---

# Os-Systemd

- During the boot, OS decides which will be the init system. 
- From the ref `The system initialization process is handled by the `init` daemon. In [squeeze](https://wiki.debian.org/DebianSqueeze) and earlier releases, that daemon is provided by the sysvinit package, and no alternatives are supported. In [wheezy](https://wiki.debian.org/DebianWheezy), the default init daemon is still sysvinit, but a "technology preview" of [systemd](https://wiki.debian.org/systemd) is available. In [jessie](https://wiki.debian.org/DebianJessie) and [stretch](https://wiki.debian.org/DebianStretch), the default init system is [systemd](https://wiki.debian.org/systemd), but switching to sysvinit is supported.`
- Ref: https://wiki.debian.org/Init
- To change that in GCE, I had to reboot the machine