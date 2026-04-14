## ADDED Requirements

### Requirement: Category sidebar displays article counts
The system SHALL display a sidebar with category filters showing the number of articles in each category.

#### Scenario: Display all categories with counts
- **WHEN** user views comments.html
- **THEN** system shows categories: 全部, 日常, 技术, 资源, 提问, 公告, 灵感
- **AND** each category shows the count of articles in that category in parentheses

#### Scenario: "全部" shows total count
- **WHEN** user views comments.html
- **THEN** "全部" shows total number of all articles

### Requirement: Category filtering works on click
The system SHALL filter the article list when user clicks a category in the sidebar.

#### Scenario: Filter by category
- **WHEN** user clicks a category (e.g., "技术")
- **THEN** only articles with that category are displayed
- **AND** the clicked category is highlighted as active

#### Scenario: Reset to all articles
- **WHEN** user clicks "全部"
- **THEN** all articles are displayed again
- **AND** "全部" is highlighted as active
