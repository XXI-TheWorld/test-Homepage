## Context

After creating a separate write.html page, the inline write form was removed from comments.html. The Form Handling IIFE that called `renderArticles()` on page load was deleted along with the form.

## Goals / Non-Goals

**Goals:**
- Restore article list rendering on comments.html page load

**Non-Goals:**
- No feature changes, only bug fix

## Decisions

Simple fix: Add `renderArticles()` call to comments.html initialization. The simplest approach is to add a document ready handler that calls `renderArticles()`.

## Risks / Trade-offs

None - this is a straightforward bug fix.
