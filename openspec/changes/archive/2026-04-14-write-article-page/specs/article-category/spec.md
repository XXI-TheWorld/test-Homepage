## MODIFIED Requirements

### Requirement: Confirm publish with no category
The system SHALL ask for confirmation when publishing with category "无".

#### Scenario: Publish with no category
- **WHEN** user clicks publish with category "无"
- **THEN** system shows confirm dialog "确定不添加标签发布吗？"
- **WHEN** user confirms
- **THEN** system publishes the article
- **WHEN** user cancels
- **THEN** system does not publish
