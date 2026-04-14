## MODIFIED Requirements

### Requirement: Submit a comment
The system SHALL automatically submit a comment using the auto-generated guest ID. Both guest_id and message fields SHALL be required.

#### Scenario: Successful comment submission
- **WHEN** visitor fills in message field and clicks submit
- **THEN** system uses the auto-generated guest_id as the comment author
- **AND** system saves the comment to localStorage linked to the article
- **AND** system clears the message input field
- **AND** system displays the new comment in the list

#### Scenario: Empty message submission
- **WHEN** visitor leaves message field empty and clicks submit
- **THEN** system displays validation error "请输入评论内容"
- **AND** comment is NOT saved
