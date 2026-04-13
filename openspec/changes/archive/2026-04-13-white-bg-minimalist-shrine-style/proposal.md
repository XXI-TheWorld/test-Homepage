## Why

当前 LinkPage 采用黑底绿色代码风格（"Matrix"美学），视觉上具有冲击力但缺乏宁静感。用户希望重新设计为日式极简风格——白色背景、大量留白、干净清爽，如同日本神社给人的感觉。这种设计转型能让页面更具普世吸引力和持久美感，而非追逐短暂的视觉潮流。

## What Changes

- 将页面背景从纯黑改为纯白
- 字体从等宽字体 (JetBrains Mono) 改为无衬线体 (如 Inter、Noto Sans JP)
- 大幅增加元素间距，引入更多垂直节奏
- 简化视觉元素，移除发光效果、阴影、装饰线
- 重新设计卡片/按钮样式，采用极简边框或纯色
- 整体布局保持简洁，大量留白，呼吸感强
- 移除所有 hover 动画效果（闪烁、发光等）

## Capabilities

### New Capabilities
- `ui-redesign`: 全面重新设计 LinkPage 的视觉风格，包括配色、字体、间距、组件样式

### Modified Capabilities
<!-- 无现有需求变更 -->

## Impact

- 修改 `index.html` 中的 CSS 样式
- 可能需要引入新的 Google Fonts（Noto Sans JP 或 Inter）
- 按钮交互效果需要重新设计（从发光转为简约的 hover 状态）
