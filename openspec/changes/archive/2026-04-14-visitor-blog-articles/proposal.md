## Why

当前评论区只能发表简短留言，无法进行更深入的交流和表达。添加访客文章功能可以让游客发表更长篇幅的内容，建立更丰富的互动社区。

## What Changes

- 新增"写文章"入口，游客可输入标题和正文内容
- 评论区列表页改为显示文章标题列表（仅标题+时间），替换原有纯留言展示
- 点击文章标题跳转到文章详情页，展示完整文章内容
- 新增"返回文章列表"链接
- 保持 localStorage 存储结构兼容

## Capabilities

### New Capabilities
- `visitor-blog`: 访客博客系统，包括文章发布、文章列表、文章详情

### Modified Capabilities
- `visitor-comments`: 评论区升级为文章列表展示，原评论功能保留文章发布能力

## Impact

- **修改页面**: `comments.html` 重构为文章列表页
- **新增页面**: `article.html` 文章详情页
- **存储结构**: localStorage 新增 `visitorArticles` 键
- **样式**: 复用现有 wood-grain 风格，保持视觉一致性
