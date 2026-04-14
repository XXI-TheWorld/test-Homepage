## Why

当前文章编辑和列表在同一页面，表单切换体验不够专注。新页面可以让用户更专注于写作。

## What Changes

- 点击"我来说两句"后跳转到新页面写文章
- 分类为"无"时发布前询问"确定不添加标签发布吗？"

## Capabilities

### New Capabilities
- `write-page`: 独立的文章编辑页面

### Modified Capabilities
- `article-category`: 分类为"无"时增加发布确认

## Impact

- 创建 write.html 页面
- 修改 comments.html 点击事件跳转
