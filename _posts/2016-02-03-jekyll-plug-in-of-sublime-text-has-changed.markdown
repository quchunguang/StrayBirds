---
layout: post
title: Jekyll plug-in of Sublime Text has changed
categories: [cs, software]
tags: [jekyll, sublime text]
published: True
comments: True
---

[User settings of sublime-jekyll][1] had totally changed.
On my Linux,

```json
{
    "jekyll_posts_path": "/home/qcg/blog/_posts",
    "jekyll_drafts_path": "/home/qcg/blog/_drafts",
    "jekyll_uploads_path": "/home/qcg/blog/_uploads"
}
```

On my Windows,

```json
{
    "jekyll_posts_path": "D:\\repos\\blog\\_posts",
    "jekyll_drafts_path": "D:\\repos\\blog\\_drafts",
    "jekyll_uploads_path": "D:\\repos\\blog\\_uploads"
}
```

Using template syntax of sublime and YAML syntax to write [Front Matter of Jekyll][2].

```yaml
---
layout: post
title:
categories: [tech]
tags: [${1}]
published: True
comments: True
---

${3}

[1]: ${2:https://www.google.com.hk/#newwindow=1&q=}
```

[1]: http://sublime-jekyll.readthedocs.org/en/latest/settings.html
[2]: http://jekyllrb.com/docs/frontmatter/
