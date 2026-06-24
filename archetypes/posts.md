+++
# =============================================================================
# 博客文章模板 — 技术分享 / 教程 / 经验总结
# 使用方式：hugo new posts/my-post/index.md --kind posts
# =============================================================================

title = '{{ replace .File.ContentBaseName "-" " " | title }}'
date = '{{ .Date }}'
draft = true
summary = ''

# 技术文章建议使用英文 kebab-case 标签，便于国际化检索。
# 参考标签：hugo, golang, python, devops, web-dev, cloud, database, ai
tags = []

# 技术文章分类固定为 tech
categories = ['tech']

# 封面图（可选）。用于列表卡片和社交分享。
# images = ['/images/posts/my-post-cover.jpg']

# 最后修改时间（可选）。内容有重要更新时建议填写。
# lastmod = ''

+++

<!--
  推荐文章结构（技术类）：

  ## 背景 / 问题
  描述你遇到了什么问题，或者这篇文章要解决什么场景。

  ## 方案 / 实现
  分步骤讲解解决方案，配合代码示例。

  ## 踩坑记录
  过程中遇到的坑和解决方式。

  ## 总结
  核心要点回顾，适用场景与局限。

  ## 参考链接
  - [链接标题](https://example.com)
-->
