---
layout: post
title: matplotlib for python not display in sublime-text editor
categories: [tech]
tags: [sublime, matplotlib]
published: True
comments: True
---

add `"shell": true` to Python.sublime-build

```json
{
    "cmd": [
        "C:\\Anaconda3\\python",
        "$file"
    ],
    "selector": "source.python",
    "file_regex": "file \"(...*?)\", line ([0-9]+)",
    "shell": true
}
```

[1]: http://stackoverflow.com/questions/10831882/matplotlib-plots-not-displaying-in-sublimetext
