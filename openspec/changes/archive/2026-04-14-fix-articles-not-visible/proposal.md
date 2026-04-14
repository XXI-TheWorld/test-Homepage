## Why

After implementing the separate write page (write.html), the "我来说两句" button now navigates to write.html instead of toggling an inline form. However, during this refactoring, the call to `renderArticles()` was accidentally removed from comments.html's initialization code, causing articles to not render on page load.

## What Changes

- Fix comments.html to call `renderArticles()` on page load
- This is a bug fix, not a feature change

## Capabilities

### Modified Capabilities
- `article-list`: Fix rendering of articles on page load (not a spec change, just implementation fix)

## Impact

- Only affects comments.html initialization
- No API or data structure changes
