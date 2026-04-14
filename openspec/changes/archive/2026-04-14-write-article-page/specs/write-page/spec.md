## ADDED Requirements

### Requirement: Write article in new page
The system SHALL open a new page for writing articles when user clicks "我来说两句".

#### Scenario: Navigate to write page
- **WHEN** user clicks "我来说两句" button
- **THEN** system navigates to write.html

### Requirement: Publish article from new page
The system SHALL allow users to publish articles from the write page.

#### Scenario: Publish article
- **WHEN** user fills in title, selects category, writes content and clicks publish
- **THEN** system saves the article
- **AND** navigates back to comments.html

#### Scenario: Back to list
- **WHEN** user clicks back button on write page
- **THEN** system navigates to comments.html
