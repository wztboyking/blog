---
layout: post
title: "jekyllbootstrap error"
description: ""
category:
tags: []
---
{% include JB/setup %}

### 问题
The page build failed with the following error:

The submodule `_theme_packages/the-program` was not properly initialized with a `.gitmodules` file. For more information, see https://help.github.com/articles/page-build-failed-missing-submodule.

If you have any questions you can contact us by replying to this email.


### 解决办法
  git rm -r --cached _theme_packages
  然后在 .gitignore 加入 _theme_packages 文件夹:
  <pre>
    *.swp
    _site
    _theme_packages
  </pre>
  Finally, commit and push to GitHub
