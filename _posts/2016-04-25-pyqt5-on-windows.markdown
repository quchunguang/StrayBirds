---
layout: post
title: pyqt5 on windows
categories: [tech]
tags: [PyQt5, Qt, python]
published: True
comments: True
---

We can develop Qt 5.6 program on windows without Qt installed.
Just install Python 3.x 32-bit (PyQt5 not support Python 2.x), make bin/ and Script/ in $PATH. And then install PyQt5 from pip3.

```bash
pip install PyQt5
```

Run PyQt program from CLI.

```
python test.py
```

Note: Run PyQt5 program from sublime directly by <kbd>ctrl</kbd>+<kbd>b</kbd> has problem (cause the python process no response) on windows. But works fine on Linux.
