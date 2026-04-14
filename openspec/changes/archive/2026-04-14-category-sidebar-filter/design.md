## Context

Article categories already exist in the system (日常, 技术, 资源, 提问, 公告, 灵感). Users can select a category when posting. However, there's no way to filter/view articles by category on comments.html.

## Goals / Non-Goals

**Goals:**
- Add sidebar with category filters
- Show article count per category
- Filter article list when category is clicked
- Mobile-friendly responsive design

**Non-Goals:**
- No changes to article data structure
- No backend changes
- Not implementing multi-category filter (single category at a time)

## Decisions

### 1. Sidebar Position
Position on the left side on desktop, top horizontal scrollable bar on mobile. This maintains the existing article list layout while adding filtering capability.

### 2. Category Count
Compute counts by iterating through articles on page load and storing counts in an object. Update when articles are added/deleted.

### 3. Filter Logic
- Maintain `currentFilter` state (null means "all")
- `filterArticles(category)` function filters the displayed list
- "全部" option always shows all articles and resets filter
- Filtering happens client-side on existing DOM elements or re-render

## Risks / Trade-offs

- Large article count may affect performance when filtering frequently → Mitigation: Client-side filtering is fast for typical article counts
