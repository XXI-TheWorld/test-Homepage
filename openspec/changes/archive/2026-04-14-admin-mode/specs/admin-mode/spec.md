## ADDED Requirements

### Requirement: Admin activation
The system SHALL allow activation of admin mode using a secret code.

#### Scenario: Activate admin mode with correct code
- **WHEN** visitor clicks "管理员登录" button
- **AND** enters the correct activation code
- **THEN** system sets admin_logged_in to true in localStorage
- **AND** displays "管理员" instead of the input code

#### Scenario: Activate admin mode with wrong code
- **WHEN** visitor enters incorrect activation code
- **THEN** system shows alert "激活码错误"
- **AND** admin mode is NOT activated

### Requirement: Admin UI indicator
The system SHALL display admin status in the comments section.

#### Scenario: Show admin status
- **WHEN** admin mode is activated
- **THEN** comments section shows "当前身份：管理员"
- **AND** hides the login button

### Requirement: Admin can delete any comment
The system SHALL allow admin to delete any comment regardless of author.

#### Scenario: Admin deletes comment
- **WHEN** admin clicks [删除] button on any comment
- **THEN** system removes the comment from localStorage
- **AND** re-renders the comment list

### Requirement: Regular user cannot see delete buttons
The system SHALL hide delete buttons from regular users.

#### Scenario: Regular user sees no delete buttons
- **WHEN** visitor has not activated admin mode
- **THEN** delete buttons are not displayed on any comments

### Requirement: Admin name styling
The system SHALL display "管理员" in red color.

#### Scenario: Admin name styling
- **WHEN** admin mode is active
- **AND** a comment is posted or displayed
- **THEN** the author name displays as "管理员" in red (#e53935) and bold
