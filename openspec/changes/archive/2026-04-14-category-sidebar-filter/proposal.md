## Why

Users need a way to filter articles by category to find relevant content more easily. Currently, articles have categories but there's no UI to filter them.

## What Changes

- Add a sidebar to comments.html with category filters
- Display all categories: 日常, 技术, 资源, 提问, 公告, 灵感
- Show article count next to each category name
- Clicking a category filters the article list to show only matching articles
- Clicking "全部" shows all articles
- Sidebar should be positioned on the left side of the article list

## Capabilities

### New Capabilities
- `category-filter`: Sidebar UI to filter articles by category with article counts

## Impact

- Only affects comments.html layout and rendering logic
- Requires new `filterArticles(category)` function
- Category counts computed from existing article data
