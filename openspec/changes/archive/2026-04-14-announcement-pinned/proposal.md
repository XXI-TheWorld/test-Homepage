## Why

Announcements (公告) need special visual treatment and permanent pinning to ensure important information is always visible to users. Currently, 公告 is treated like other categories.

## What Changes

- Move "公告" to top of sidebar and style it in red to stand out
- Restrict 公告 category selection to admin users only (already implemented for submission, need to ensure UI reflects this)
- Pin the most recent 公告 article permanently at the top of the article list
- The pinned announcement should always be visible regardless of category filter state

## Capabilities

### New Capabilities
- `announcement-pinned`: Display most recent announcement article permanently pinned at top
- `announcement-visibility`: Style 公告 differently in sidebar, admin-only selection

## Impact

- Only affects comments.html display and article rendering
- Requires checking article category and timestamp for pinning logic
- Admin-only category selection already exists in write.html
