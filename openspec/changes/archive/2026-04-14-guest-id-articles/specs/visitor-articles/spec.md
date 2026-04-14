## MODIFIED Requirements

### Requirement: Publish an article
The system SHALL automatically publish articles using the visitor's guest ID as the author. Visitors do not need to enter a nickname.

#### Scenario: Publish article with auto guest ID
- **WHEN** visitor fills in title and content and clicks publish
- **THEN** system uses the visitor's guest ID as the article author
- **AND** system saves the article to localStorage
- **AND** system displays the new article in the list

#### Scenario: Empty content validation
- **WHEN** visitor leaves title or content empty and clicks publish
- **THEN** system displays validation error
- **AND** article is NOT saved
