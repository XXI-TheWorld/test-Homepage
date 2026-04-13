## ADDED Requirements

### Requirement: WeChat ID copy button
The system SHALL provide a button that allows users to copy the WeChat ID to the system clipboard when clicked.

#### Scenario: Successful copy
- **WHEN** user clicks the "Copy WeChat ID" button
- **THEN** the WeChat ID SHALL be copied to the clipboard
- **AND** a "已复制 ✓" (copied) message SHALL be displayed temporarily

#### Scenario: Copy feedback disappears
- **WHEN** the "已复制 ✓" message is displayed
- **THEN** it SHALL automatically disappear after 2 seconds
