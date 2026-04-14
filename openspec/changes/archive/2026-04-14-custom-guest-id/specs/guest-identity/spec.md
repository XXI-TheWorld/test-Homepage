## MODIFIED Requirements

### Requirement: Modify guest ID
The system SHALL allow visitors to modify their guest ID to a custom name of 1-15 characters (Chinese or English).

#### Scenario: Modify guest ID with valid name
- **WHEN** visitor clicks "修改身份" button
- **THEN** system prompts for new ID with character limit of 15
- **WHEN** visitor enters a valid name (1-15 characters) that is not already in use
- **THEN** system saves the new ID to localStorage
- **AND** system updates the displayed identity

#### Scenario: Duplicate ID rejection
- **WHEN** visitor enters a name that is already in use by another user
- **THEN** system displays alert "该名称已被占用"
- **AND** ID is NOT changed

#### Scenario: Cancel modify
- **WHEN** visitor clicks "修改身份" button
- **AND** cancels the prompt
- **THEN** system keeps the existing guest ID

#### Scenario: Invalid length
- **WHEN** visitor enters a name shorter than 1 or longer than 15 characters
- **THEN** system shows validation error
- **AND** ID is NOT changed
