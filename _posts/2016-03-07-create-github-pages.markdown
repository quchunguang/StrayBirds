---
layout: post
title: create github pages
categories: [tech]
tags: [github pages, git]
published: True
comments: True
---

```bash
git clone github.com/user/repository.git
cd repository

# Creates our branch, without any parents (it's an orphan!)
git checkout --orphan gh-pages

# Remove all files from the old working tree
git rm -rf .
rm '.gitignore'

# Add content and push
echo "My Page" > index.html
git add index.html
git commit -a -m "First pages commit"
git push origin gh-pages

# Access page at
x-www-browser http(s)://<username>.github.io/<projectname>
```

[1]: https://help.github.com/articles/creating-project-pages-manually/
