## MODIFIED Requirements

### Requirement: Delete own article
The system SHALL allow visitors to delete their own articles using their current guest ID for verification. No additional nickname input is required.

#### Scenario: Delete own article
- **WHEN** visitor clicks delete on an article they authored (matched by guest ID)
- **THEN** system displays a confirmation dialog "确定删除这篇文章吗？"
- **WHEN** visitor confirms the deletion
- **THEN** system removes the article from localStorage
- **AND** system redirects to the article list page

#### Scenario: Cannot delete others' articles
- **WHEN** visitor clicks delete on an article authored by a different guest ID
- **THEN** system does not show delete button
