## ADDED Requirements

### Requirement: Visit counter
The system SHALL display a visit counter at the bottom of the page showing the number of times the page has been visited.

#### Scenario: Counter increments on page load
- **WHEN** the page loads
- **THEN** the visit count SHALL be retrieved from localStorage
- **AND** the count SHALL be incremented by 1
- **AND** the new count SHALL be saved to localStorage
- **AND** the count SHALL be displayed at the bottom of the page
