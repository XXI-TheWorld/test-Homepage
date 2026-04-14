## Why

需要一个纯前端的"本地管理员模式"，用于管理和删除任意评论，无需后端数据库支持。

## What Changes

- 设定管理员激活暗号（如 admin123）
- 输入暗号后，显示为"管理员"而非原始输入
- localStorage 标记管理员状态
- 管理员模式下，所有评论显示红色删除按钮
- 管理员名字使用特殊样式（红色）区分普通用户

## Capabilities

### New Capabilities
- `admin-mode`: 本地管理员模式，支持激活管理员状态和删除任意评论

### Modified Capabilities
- `comment-render`: 管理员模式下显示删除按钮，普通用户不显示

## Impact

- 修改 article.html 中评论渲染逻辑
- 修改 localStorage 使用方式（新增 admin_logged_in 键）
