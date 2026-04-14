## MODIFIED Requirements

### Requirement: Delete own comment
The system SHALL allow visitors to delete their own comments using their current guest ID for verification. No additional nickname input is required.

#### Scenario: Delete own comment
- **WHEN** visitor clicks delete on a comment they authored (matched by guest ID)
- **THEN** system displays a confirmation dialog "确定删除这条评论吗？"
- **WHEN** visitor confirms the deletion
- **THEN** system removes the comment from the article's comments array in localStorage

#### Scenario: Cannot delete others' comments
- **WHEN** visitor clicks delete on a comment authored by a different guest ID
- **THEN** system does not show delete button
