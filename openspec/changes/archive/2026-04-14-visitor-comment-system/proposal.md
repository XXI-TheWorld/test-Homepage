## Why

当前页面缺少访客互动功能，访客只能被动浏览链接而无法留言互动。添加评论系统可以让访客留下反馈、问候或交流，增强社区感和用户粘性。

## What Changes

- 新增"评论区"链接按钮，点击跳转至评论区页面
- 评论区页面展示所有访客留言，显示头像、名称、时间和内容
- 访客可自由输入昵称和留言内容进行评论
- 评论数据通过 localStorage 本地存储，实现持久化

## Capabilities

### New Capabilities
- `visitor-comments`: 游客评论系统，包括评论列表展示、评论输入、头像生成、数据持久化

### Modified Capabilities
- (无)

## Impact

- **新增页面**: `comments.html` 评论区页面
- **修改文件**: `index.html` 新增评论区跳转按钮
- **新增文件**: `js/comments.js` 评论功能逻辑
- **样式**: 复用现有 wood-grain 风格，保持视觉一致性
