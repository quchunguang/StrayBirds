---
layout: post
title: Masonry grid float template for Bootstrap
categories: [tech]
tags: [masonry, bootstrap, jquery]
published: True
comments: True
---

Reference sample at [masonry_bootstrap.html](http://github.com/quchunguang/test/blob/master/testjs/masonry_bootstrap.html) and [Official document][1].

```html
<div class="container-fluid">
  <!-- add extra container element for Masonry -->
  <div class="grid">
    <!-- add sizing element for columnWidth -->
    <div class="grid-sizer col-xs-4"></div>
    <!-- items use Bootstrap .col- classes -->
    <div class="grid-item col-xs-8">
      <!-- wrap item content in its own element -->
      <div class="grid-item-content">...</div>
    </div>
    <div class="grid-item col-xs-4">
      <div class="grid-item-content">...</div>
    </div>
    ...
  </div>
</div>
```

```js
$('.grid').masonry({
  itemSelector: '.grid-item', // use a separate class for itemSelector, other than .col-
  columnWidth: '.grid-sizer',
  percentPosition: true
});
```

[1]: http://masonry.desandro.com/extras.html
