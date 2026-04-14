## ADDED Requirements

### Requirement: Visitor can view comments list
The system SHALL display a list of all saved comments, showing each comment's avatar, nickname, timestamp, and content. Comments SHALL be displayed in reverse chronological order (newest first).

#### Scenario: Display existing comments
- **WHEN** user navigates to the comments page
- **THEN** system retrieves all comments from localStorage and renders them in a scrollable list
- **AND** each comment displays: generated avatar, nickname, relative time (e.g., "2小时前"), and message content

#### Scenario: Empty comments state
- **WHEN** user navigates to comments page with no saved comments
- **THEN** system displays an empty state message encouraging visitors to leave the first comment

### Requirement: Visitor can submit a comment
The system SHALL allow visitors to submit a comment by entering a nickname and message content. Both fields SHALL be required.

#### Scenario: Successful comment submission
- **WHEN** visitor fills in both nickname and message fields and clicks submit
- **THEN** system saves the comment to localStorage with a generated avatar, current timestamp, and unique ID
- **AND** system clears the input fields
- **AND** system displays the new comment at the top of the list

#### Scenario: Empty nickname submission
- **WHEN** visitor leaves nickname field empty and clicks submit
- **THEN** system displays a validation error "请输入昵称"
- **AND** comment is NOT saved

#### Scenario: Empty message submission
- **WHEN** visitor fills in nickname but leaves message empty and clicks submit
- **THEN** system displays a validation error "请输入留言内容"
- **AND** comment is NOT saved

### Requirement: Avatar generation from nickname
The system SHALL generate a unique avatar for each nickname using the first 1-2 characters of the nickname. Avatar background color SHALL be derived from a hash of the nickname to ensure consistency for the same nickname.

#### Scenario: Avatar generation
- **WHEN** a comment is saved with nickname "小明"
- **THEN** system generates an avatar displaying "小" in a square with rounded corners
- **AND** the background color is consistent for "小明" across all page visits

### Requirement: Comment timestamp display
The system SHALL display comment timestamps in a human-readable relative format (e.g., "刚刚", "5分钟前", "2小时前", "3天前").

#### Scenario: Recent comment timestamp
- **WHEN** comment is posted within 1 minute
- **THEN** display "刚刚"

#### Scenario: Hour-old comment timestamp
- **WHEN** comment was posted more than 1 minute but less than 1 hour ago
- **THEN** display "X分钟前"

#### Scenario: Day-old comment timestamp
- **WHEN** comment was posted more than 24 hours but less than 7 days ago
- **THEN** display "X天前"

#### Scenario: Week-old comment timestamp
- **WHEN** comment was posted more than 7 days ago
- **THEN** display the exact date in format "YYYY-MM-DD"
