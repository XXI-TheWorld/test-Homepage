## Why

游客每次访问都需要手动输入昵称，体验割裂且容易遗忘。自动生成唯一游客 ID 并持久化存储，可以简化操作流程，同时保持游客身份的连续性。

## What Changes

- 新增游客 ID 持久化机制（4 位数字，localStorage 存储）
- 页面加载时自动读取或生成游客 ID
- 评论区顶部显示"当前身份：XXXX"，而非输入框
- 发表评论时自动使用该 ID，无需手动输入

## Capabilities

### New Capabilities
- `guest-identity`: 自动生成并持久化游客身份标识，页面加载时自动恢复身份

### Modified Capabilities
- `article-comments`: 评论提交时使用自动游客 ID，不再需要手动输入昵称

## Impact

- 修改 `article.html` 中的评论表单 UI 和提交逻辑
- localStorage 新增 `guest_id` 键值存储
