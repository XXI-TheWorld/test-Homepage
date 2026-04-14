## Why

当前 guest ID 是 4 位数字，限制较多且不直观。游客希望能使用更有意义的自定义名称（中英文均可），同时需要确保 ID 的唯一性避免混淆。

## What Changes

- Guest ID 从 4 位数字改为最多 15 个中/英文字符的自定义名称
- 检查 ID 唯一性，不允许使用已被占用的名称
- 重复 ID 提示"该名称已被占用"

## Capabilities

### Modified Capabilities
- `guest-identity`: 支持自定义名称（最多 15 字符），增加 ID 唯一性校验

## Impact

- 修改 localStorage 中 guest_id 的存储格式
- 修改所有使用 guest_id 的显示逻辑
- 新增 ID 唯一性检查函数
