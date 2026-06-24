+++
# =============================================================================
# 博客文章模板 — 技术分享 / 教程 / 经验总结
# 使用方式：hugo new posts/my-post/index.md --kind posts
# =============================================================================

title = 'Hello World — 我的 Hugo 博客搭建之旅'
date = '2026-06-24T08:43:21+08:00'
draft = false
summary = '从零开始用 Hugo 搭建个人博客的完整记录。'

# 技术文章建议使用英文 kebab-case 标签，便于国际化检索。
# 参考标签：hugo, golang, python, devops, web-dev, cloud, database, ai
tags = ['hugo', 'tutorial', 'blog']

# 技术文章分类固定为 tech
categories = ['tech']
lastmod = '2026-06-24T15:00:00+08:00'
keywords = ['Hugo 博客', '静态网站']
images = ['/images/posts/hello-world/cover.png']

# 封面图（可选）。用于列表卡片和社交分享。
# images = ['/images/posts/my-post-cover.jpg']

# 最后修改时间（可选）。内容有重要更新时建议填写。
# lastmod = ''

+++

<!--
  示例文章 — 展示 Front Matter、标签、Shortcode 的综合使用
-->

## 为什么要写博客？

在信息爆炸的时代，**写作是最好的思考方式**。搭建个人博客不是为了追逐流量，而是：

- 📝 **知识沉淀** — 把碎片化的学习整理成体系
- 🤝 **与人交流** — 分享观点，收获反馈
- 🏗️ **积累数字资产** — 一个完全由自己掌控的网络空间

我选择 [Hugo](https://gohugo.io) 是因为它 **极快的构建速度**、**灵活的内容管理**，以及 **丰富的主题生态**。

---

## 技术选型

| 组件 | 选择 | 理由 |
|------|------|------|
| 静态生成器 | Hugo | Go 编写，构建速度 < 1s |
| 主题 | hugo-trainsh | 极简风、支持三色主题切换 |
| 部署 | Cloudflare Pages | 免费、全球 CDN |

---

## 使用 archetype 创建文章

```bash
# 技术文章 — 自动使用 archetypes/posts.md 模板
hugo new content posts/my-article.md

# 生活随笔 — 使用 archetypes/notes.md
hugo new content notes/my-note.md

# 读书笔记 — 使用 archetypes/books.md
hugo new content books/my-book.md

hugo server -D  # 本地预览
```

---

## 有用的 Shortcode 提示

{{< notice tip >}}
**开发技巧**：使用 `hugo server -D --navigateToChanged` 可以在编辑文件后自动刷新浏览器并导航到对应页面。
{{< /notice >}}

{{< notice warning >}}
**注意**：部署前记得把 `draft = false`，否则草稿文章不会出现在生产构建中。
{{< /notice >}}

---

## 标签体系设计

我设计了一套**二维分类体系**来组织文章：

- **categories（分类）**：纵向维度，定义内容归属的大类。一篇文章只属于一个分类 — `tech` / `life` / `reading`
- **tags（标签）**：横向维度，标注具体的主题关键词。一篇文章可以有多个标签 — 如 `hugo`, `golang`, `日常`

完整的标签层次结构请参考项目中的标签体系文档。

---

## 代码块示例

Go：

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, Hugo Blog!")
}
```

Python：

```python
def count_tags(articles):
    """统计所有标签出现次数"""
    tags = {}
    for a in articles:
        for t in a.get("tags", []):
            tags[t] = tags.get(t, 0) + 1
    return tags
```

---

## 下一步计划

- [ ] 绑定自定义域名
- [ ] 添加评论系统（Giscus）
- [ ] 撰写更多文章 🚀

---

## 参考链接

- [Hugo 官方文档](https://gohugo.io/documentation/)
- [hugo-trainsh 主题](https://github.com/binbinsh/hugo-trainsh)
- [Cloudflare Pages 文档](https://developers.cloudflare.com/pages/)
