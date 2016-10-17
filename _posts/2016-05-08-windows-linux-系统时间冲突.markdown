---
layout: post
title: Windows Linux 系统时间冲突
categories: [tech]
tags: []
published: True
comments: True
---

```
# Windows
regedit
In HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\TimeZoneInformation
Add DWORD RealTimeIsUniversal=1

# Or, Linux
vim /etc/default/rcS
UTC=yes -> UTC=no
```

[1]: http://blog.gtwang.org/linux/fix-time-problem-dual-boot-computers-windows-linux/
