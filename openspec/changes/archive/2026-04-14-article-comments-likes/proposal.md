## Why

当前文章系统只能发布文章，缺少互动功能。用户希望能够对文章进行评论、点赞，并删除自己发布的文章和评论，增加用户互动性和社区活跃度。

## What Changes

- 文章详情页添加评论功能：显示评论列表和评论输入框
- 评论显示游客昵称、内容、时间和头像
- 文章和评论添加点赞功能：点击点赞，再次点击取消点赞
- 游客只能删除自己发布的文章和评论
- 删除时需确认，防止误操作
- localStorage 存储结构扩展支持评论和点赞

## Capabilities

### New Capabilities
- `article-comments`: 文章评论功能
- `article-likes`: 文章和评论点赞功能
- `article-delete`: 文章和评论删除功能

### Modified Capabilities
- `visitor-blog`: localStorage 结构扩展，存储评论和点赞数据

## Impact

- **修改页面**: `article.html` - 添加评论列表、评论输入、点赞按钮、删除按钮
- **存储结构**: localStorage 新增评论列表和点赞状态
- **逻辑**: 游客身份识别（通过昵称）用于删除和点赞权限控制
