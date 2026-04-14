## ADDED Requirements

### Requirement: Display comments for an article
The system SHALL display a list of comments for each article, showing the comment author's avatar, nickname, timestamp, and content. Comments SHALL be displayed in chronological order (oldest first).

#### Scenario: Display comments list
- **WHEN** user navigates to an article detail page
- **THEN** system retrieves comments for that article from localStorage
- **AND** displays each comment with avatar, nickname, relative time, and content
- **AND** comments are shown in chronological order (oldest first)

#### Scenario: Empty comments state
- **WHEN** user navigates to an article with no comments
- **THEN** system displays "还没有评论" message

### Requirement: Submit a comment
The system SHALL allow visitors to submit a comment by entering a nickname and message content. Both fields SHALL be required.

#### Scenario: Successful comment submission
- **WHEN** visitor fills in nickname and message fields and clicks submit
- **THEN** system saves the comment to localStorage linked to the article
- **AND** system clears the input fields
- **AND** system displays the new comment in the list

#### Scenario: Empty nickname submission
- **WHEN** visitor leaves nickname field empty and clicks submit
- **THEN** system displays validation error "请输入昵称"
- **AND** comment is NOT saved

#### Scenario: Empty message submission
- **WHEN** visitor fills in nickname but leaves message empty and clicks submit
- **THEN** system displays validation error "请输入评论内容"
- **AND** comment is NOT saved

### Requirement: Comment avatar generation
The system SHALL generate a unique avatar for each comment author using the first character of the nickname. Avatar background color SHALL be derived from a hash of the nickname.

#### Scenario: Comment avatar
- **WHEN** a comment is saved with nickname "小明"
- **THEN** system generates an avatar displaying "小" with a color based on nickname hash
