## Why

当前文章列表页直接显示写文章表单，页面加载时就占用空间。用户希望先看到文章列表，通过点击"我来说两句"按钮才展开写作界面，改善用户体验。同时用户反馈页面太窄，需要加宽。

## What Changes

- 页面底部添加"我来说两句"按钮
- 写文章表单默认隐藏，点击按钮后展开显示
- 再次点击按钮或提交后表单隐藏
- 页面容器宽度从 520px 增加到 960px

## Capabilities

### New Capabilities
- `write-form-toggle`: 写作表单的显示/隐藏切换功能

### Modified Capabilities
- `visitor-blog`: 表单默认隐藏，通过按钮触发显示

## Impact

- **修改页面**: `comments.html` - 添加切换按钮，修改容器宽度
- **影响**: 表单交互逻辑变化，CSS 宽度调整
