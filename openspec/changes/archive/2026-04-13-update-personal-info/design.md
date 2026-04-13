## Context

LinkPage 需要替换为用户的真实个人信息。这是一个简单的数据替换变更，不涉及架构调整。

## Goals / Non-Goals

**Goals:**
- 更新用户名字为 "The World"
- 更新简介为 "欢迎来到我的主页"
- 更新 Bilibili 链接为真实主页 URL
- 更新微信号为 "18622859870"
- 更换背景音乐为和风三味线轻音乐

**Non-Goals:**
- 不改变页面布局和视觉风格
- 不添加或移除任何功能

## Decisions

### 1. 用户信息替换
- 名字：`<h1 class="name">The World</h1>`
- 简介：`<p class="bio">欢迎来到我的主页</p>`
- 微信号硬编码：`const wechatId = '18622859870';`

### 2. Bilibili 链接
- URL：`https://space.bilibili.com/3363942?spm_id_from=333.40164.0.0`
- 替换现有的占位链接

### 3. 背景音乐
- 和风三味线轻音乐
- 使用公开可用的音乐 URL（需用户提供或搜索）
- 保持现有的播放控制逻辑

## Risks / Trade-offs

| 风险 | Mitigation |
|------|------------|
| 音乐 URL 可能失效 | 使用可靠的公开音乐托管服务 |

## Open Questions

- 和风三味线音乐的来源 URL 是什么？
