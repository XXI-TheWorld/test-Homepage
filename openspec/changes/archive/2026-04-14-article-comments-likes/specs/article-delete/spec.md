## ADDED Requirements

### Requirement: Delete own article
The system SHALL allow visitors to delete their own articles. A visitor can only delete articles where the article's nickname matches the visitor's current nickname.

#### Scenario: Delete own article
- **WHEN** visitor enters their nickname and clicks delete on an article they authored
- **THEN** system displays a confirmation dialog "确定删除这篇文章吗？"
- **WHEN** visitor confirms the deletion
- **THEN** system removes the article from localStorage
- **AND** system redirects to the article list page

#### Scenario: Delete verification
- **WHEN** visitor clicks delete button on an article
- **THEN** system prompts for nickname input to verify ownership
- **IF** nickname matches article author
- **THEN** system shows confirmation dialog
- **ELSE** system shows error "无法删除：这不是你的文章"

### Requirement: Delete own comment
The system SHALL allow visitors to delete their own comments. A visitor can only delete comments where the comment's nickname matches the visitor's current nickname.

#### Scenario: Delete own comment
- **WHEN** visitor enters their nickname and clicks delete on a comment they authored
- **THEN** system displays a confirmation dialog "确定删除这条评论吗？"
- **WHEN** visitor confirms the deletion
- **THEN** system removes the comment from the article's comments array in localStorage

#### Scenario: Delete verification
- **WHEN** visitor clicks delete button on a comment
- **THEN** system prompts for nickname input to verify ownership
- **IF** nickname matches comment author
- **THEN** system shows confirmation dialog
- **ELSE** system shows error "无法删除：这不是你的评论"

### Requirement: Delete button visibility
The system SHALL only show the delete button on articles and comments that the current visitor has authored.

#### Scenario: Show delete button for own content
- **WHEN** visitor enters their nickname on an article/detail page
- **THEN** system shows delete button on articles and comments matching that nickname

#### Scenario: Hide delete button for others' content
- **WHEN** visitor has not entered a nickname or entered a different nickname
- **THEN** system hides the delete button on all content
