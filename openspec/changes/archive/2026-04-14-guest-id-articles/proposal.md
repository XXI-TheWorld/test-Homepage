## Why

当前游客写文章需要手动输入昵称，与评论系统的自动 guest ID 体验不一致。游客也无法修改自己的 ID。删除文章/评论时的昵称确认流程可以简化。

## What Changes

- 写文章时直接使用自动分配的 guest ID，无需手动输入
- 文章作者可以删除自己的文章（通过 guest ID 验证）
- 游客可以修改自己的 guest ID
- 删除文章/评论时不再询问昵称，使用已知的 guest ID 进行验证

## Capabilities

### New Capabilities
- `guest-id-modify`: 允许游客修改自己的 guest ID

### Modified Capabilities
- `visitor-articles`: 写文章时使用 guest ID，无需手动输入昵称
- `article-delete`: 删除文章时使用已知 guest ID 验证，无需额外询问
- `comment-delete`: 删除评论时使用已知 guest ID 验证，无需额外询问

## Impact

- 修改 `index.html` 中文章发布表单
- 修改 `article.html` 中删除确认逻辑
- localStorage 的 `guest_id` 键值需要支持更新
