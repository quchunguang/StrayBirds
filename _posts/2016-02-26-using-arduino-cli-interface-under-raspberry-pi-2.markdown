---
layout: post
title: using arduino cli interface under raspberry pi 2
categories: [tech]
tags: [arduino, raspberry]
published: True
comments: True
---

```bash
apt-get install arduino-core

# apt-get install arduino-mk
# BUG: Instead of above line, copy https://github.com/quchunguang/homemake/blob/master/arduino.mk to `$ARDUINO_ROOT`, the root of arduino projects. And, for example, a project named `led` located in $ARDUINO_ROOT/led/, create Makefile,

```mk
BOARD = uno
include ../arduino.mk
```

Then run `make upload` to make and upload to Arduino connected with raspberry pi 2.
