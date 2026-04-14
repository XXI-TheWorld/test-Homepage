## ADDED Requirements

### Requirement: Visitor can write an article
The system SHALL allow visitors to write and submit an article by entering a title and body content. Both title and body fields SHALL be required. Title SHALL be limited to 100 characters, body SHALL be limited to 10000 characters.

#### Scenario: Successful article submission
- **WHEN** visitor fills in both title and body fields and clicks submit
- **THEN** system saves the article to localStorage with a generated avatar, current timestamp, and unique ID
- **AND** system clears the input fields
- **AND** system redirects to the article list page

#### Scenario: Empty title submission
- **WHEN** visitor leaves title field empty and clicks submit
- **THEN** system displays a validation error "请输入文章标题"
- **AND** article is NOT saved

#### Scenario: Empty body submission
- **WHEN** visitor fills in title but leaves body empty and clicks submit
- **THEN** system displays a validation error "请输入文章内容"
- **AND** article is NOT saved

#### Scenario: Title exceeds character limit
- **WHEN** visitor enters a title with more than 100 characters
- **THEN** system prevents further input beyond 100 characters

### Requirement: Visitor can view article list
The system SHALL display a list of all published articles, showing each article's title and timestamp. Articles SHALL be displayed in reverse chronological order (newest first).

#### Scenario: Display article list
- **WHEN** user navigates to the articles page
- **THEN** system retrieves all articles from localStorage and renders them in a scrollable list
- **AND** each article displays: title (as clickable link) and relative timestamp

#### Scenario: Empty articles state
- **WHEN** user navigates to articles page with no saved articles
- **THEN** system displays an empty state message encouraging visitors to write the first article

### Requirement: Visitor can view article detail
The system SHALL display the full article content when user clicks on an article title. The article detail page SHALL show title, author avatar, author nickname, timestamp, and body content.

#### Scenario: View article detail
- **WHEN** user clicks on an article title in the list
- **THEN** system navigates to article.html with the article ID as URL parameter
- **AND** system retrieves and displays the full article content

#### Scenario: Article not found
- **WHEN** user navigates to article.html with an invalid or missing article ID
- **THEN** system displays an error message "文章不存在或已被删除"
- **AND** system provides a link back to the article list

### Requirement: Article timestamp display
The system SHALL display article timestamps in a human-readable relative format (e.g., "刚刚", "5分钟前", "2小时前", "3天前"). For articles older than 7 days, display the exact date in format "YYYY-MM-DD".

#### Scenario: Recent article timestamp
- **WHEN** article is posted within 1 minute
- **THEN** display "刚刚"

#### Scenario: Week-old article timestamp
- **WHEN** article is posted more than 7 days ago
- **THEN** display the exact date in format "YYYY-MM-DD"

### Requirement: Avatar generation from author nickname
The system SHALL generate a unique avatar for each author using the first 1-2 characters of the nickname. Avatar background color SHALL be derived from a hash of the nickname to ensure consistency.

#### Scenario: Avatar generation
- **WHEN** an article is saved with nickname "小明"
- **THEN** system generates an avatar displaying "小" in a rounded square
- **AND** the background color is consistent for "小明" across all page visits
