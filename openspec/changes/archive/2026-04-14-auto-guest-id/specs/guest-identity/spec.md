## ADDED Requirements

### Requirement: Auto-generate guest ID
The system SHALL generate a unique 4-digit guest ID when no guest_id exists in localStorage.

#### Scenario: Generate new guest ID
- **WHEN** page loads and localStorage does not contain guest_id
- **THEN** system generates a random 4-digit number (1000-9999)
- **AND** saves it to localStorage under key "guest_id"
- **AND** displays "当前身份：XXXX" in the comments section

#### Scenario: Restore existing guest ID
- **WHEN** page loads and localStorage contains guest_id
- **THEN** system reads the guest_id value
- **AND** displays "当前身份：XXXX" in the comments section

### Requirement: Persistent guest identity
The system SHALL maintain the guest identity across page reloads.

#### Scenario: Identity persists after reload
- **WHEN** visitor reloads the page
- **THEN** system displays the same guest_id that was previously generated
- **AND** visitor can continue to comment with the same identity
