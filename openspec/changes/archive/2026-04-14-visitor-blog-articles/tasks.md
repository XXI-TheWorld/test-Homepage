## 1. Modify comments.html to Article List Page

- [x] 1.1 Change page title to "文章列表"
- [x] 1.2 Replace comment form with article write form (title + body inputs)
- [x] 1.3 Replace comment list with article title list (only titles as links + timestamp)
- [x] 1.4 Update empty state message to encourage writing first article
- [x] 1.5 Implement article submission: save to localStorage, redirect to article list

## 2. Create article.html Detail Page

- [x] 2.1 Create article.html with same CSS variables and wood-grain style
- [x] 2.2 Parse article ID from URL parameter (?id=xxx)
- [x] 2.3 Implement article retrieval from localStorage
- [x] 2.4 Display article title, author avatar, nickname, timestamp, and body content
- [x] 2.5 Handle "article not found" case with error message and back link

## 3. Article Display Components

- [x] 3.1 Reuse avatar generation function from existing comments.js
- [x] 3.2 Reuse timestamp formatting function (relative time)
- [x] 3.3 Style article title as clickable link with hover effect
- [x] 3.4 Style article content with proper typography (line-height, word-break)

## 4. Theme Consistency

- [x] 4.1 Apply same dark/light theme toggle functionality
- [x] 4.2 Ensure wood-grain borders and colors match existing style
- [x] 4.3 Add back navigation link to return to article list page

## 5. localStorage Integration

- [x] 5.1 Implement localStorage save/load functions for articles
- [x] 5.2 Store articles with id, title, body, nickname, timestamp, avatar color
- [x] 5.3 Load articles in reverse chronological order
