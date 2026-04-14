## Why

让文章可以按分类筛选和浏览，提升用户体验。

## What Changes

- 发文章时可以选择分类：日常、技术、资源、提问、公告、灵感，默认"无"
- "公告"分类只有管理员能选择
- 文章列表和详情页显示分类标签

## Capabilities

### New Capabilities
- `article-category`: 文章分类功能，支持选择分类，管理员独占公告分类

### Modified Capabilities
- `visitor-articles`: 发布文章时增加分类选择

## Impact

- 修改 comments.html 文章发布表单
- 修改 comments.html 文章列表渲染
- 修改 article.html 文章详情页显示
