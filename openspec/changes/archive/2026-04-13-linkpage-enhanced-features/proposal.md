## Why

LinkPage 当前缺乏用户交互功能和个性化设置能力。用户需要：复制微信号方便联系、外链新标签打开不打断浏览、深色模式适配不同场景、访问计数满足好奇心、背景音乐营造氛围。

## What Changes

- 添加「复制微信号」按钮，点击后复制微信号并显示"已复制"提示
- 所有外链添加 `target="_blank"` 在新标签页打开
- 页面右上角添加深色/浅色模式切换按钮，带平滑过渡动画
- 页面底部添加访问计数器，使用 localStorage 记录
- 添加音乐播放按钮，可播放/暂停背景音乐，默认静音

## Capabilities

### New Capabilities
- `wechat-copy`: 复制微信号功能，包含剪贴板操作和用户反馈
- `dark-mode-toggle`: 深色/浅色模式切换功能
- `visit-counter`: localStorage 访问计数
- `background-music`: 背景音乐播放控制

## Impact

- 修改 `index.html` 中的 HTML 结构（新增按钮元素）
- 修改 CSS（深色模式变量、过渡动画、新按钮样式）
- 添加 JavaScript 功能逻辑
- 需要一个背景音乐文件或使用公开可用的音乐 URL
