## ADDED Requirements

### Requirement: Select article category
The system SHALL allow visitors to select a category when publishing an article.

#### Scenario: Select category when publishing
- **WHEN** visitor fills in title and content and selects a category
- **THEN** system saves the article with the selected category
- **AND** displays the category on article list and detail page

#### Scenario: Default category
- **WHEN** visitor does not select any category
- **THEN** system defaults to "无" category

#### Scenario: Admin-only announcement category
- **WHEN** non-admin visitor selects "公告" category
- **THEN** system shows alert "只有管理员才能选择此分类"
- **AND** does not save the article with this category

### Requirement: Display article category
The system SHALL display the category on article list and detail page.

#### Scenario: Display category tag
- **WHEN** article has a category other than "无"
- **THEN** system displays category tag next to title
- **WHEN** article has category "无"
- **THEN** no category tag is displayed
