---
layout: post
title: install LXQt on lubuntu
categories: [tech]
tags: [LXQt, Lubuntu, LXDE]
published: True
comments: True
---

Sadly, LXQt still not default on Lubuntu 16.04.
Install LXQt instead of LXDE to an existing Lubuntu.

```bash
sudo sed -i "s/xenial/devel/g" /etc/apt/sources.list
sudo add-apt-repository -y ppa:tsimonq2/lxqt-meta
sudo apt update
sudo apt install -y lxqt-metapackage lxqt-common
sudo apt purge light-locker xfce4-power-manager
```

[1]: https://wiki.ubuntu.com/Lubuntu/LXQt
