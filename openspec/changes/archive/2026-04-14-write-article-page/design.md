## Context

当前文章编辑在评论列表页的折叠表单中，切换不够流畅。

## Goals / Non-Goals

**Goals:**
- 独立写文章页面
- 分类为"无"时发布确认

**Non-Goals:**
- 不改变现有文章数据存储结构
- 不实现文章编辑功能

## Decisions

### 1. 跳转方式
点击"我来说两句"时直接跳转 `write.html`，不再使用折叠表单。

### 2. 页面内容
新页面包含：标题输入、分类选择、内容输入、发布按钮。

### 3. 发布后跳转
发布成功后跳转到 comments.html 列表页。

## Risks / Trade-offs

- 需要新建 write.html 页面文件
