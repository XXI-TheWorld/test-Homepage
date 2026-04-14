## Context

The sidebar already exists with category filters. The 公告 category already has admin-only restrictions in write.html. Now we need to:
1. Style 公告 in sidebar with red color and position at top
2. Add pinned announcement display at top of article list

## Goals / Non-Goals

**Goals:**
- 公告 item in sidebar is red and positioned first
- Latest 公告 article always shows at top of list regardless of filter
- Non-admin users cannot see or select 公告 in sidebar

**Non-Goals:**
- No changes to write.html (admin check already exists)
- Not implementing multiple pinned items

## Decisions

### 1. Sidebar Styling
Use CSS class `.category-item.announcement` with red background/text to highlight 公告. On desktop, render 公告 first in the list. Hide from non-admin users via `isAdmin()` check.

### 2. Pinned Announcement Logic
- Find the article with most recent timestamp where `category === '公告'`
- Prepend this article to the rendered list BEFORE other articles
- If no announcements exist, don't show pinned section
- The pinned item should have distinct styling (larger, different border)

## Risks / Trade-offs

- Pinned announcement shows regardless of current category filter → This is intentional for visibility
- If announcement is deleted, the pinned slot simply disappears
