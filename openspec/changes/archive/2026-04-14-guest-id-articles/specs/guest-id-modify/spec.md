## ADDED Requirements

### Requirement: Modify guest ID
The system SHALL allow visitors to modify their guest ID.

#### Scenario: Modify guest ID
- **WHEN** visitor clicks "修改身份" button
- **THEN** system prompts for new 4-digit ID
- **WHEN** visitor enters a 4-digit number (1000-9999) and confirms
- **THEN** system saves the new ID to localStorage
- **AND** system updates the displayed identity

#### Scenario: Cancel modify
- **WHEN** visitor clicks "修改身份" button
- **AND** cancels the prompt
- **THEN** system keeps the existing guest ID
