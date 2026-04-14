## ADDED Requirements

### Requirement: Background music on comments page
The system SHALL play background music on the comments page using the same audio file as the main page (`./music/Sakura.mp3`).

#### Scenario: Music control button visible
- **WHEN** user navigates to the comments page
- **THEN** system displays a music control button in the bottom-right corner
- **AND** button shows current play state (▶ or ⏸)

### Requirement: Music playback state sync
The system SHALL sync music playback state with localStorage so music continues playing when navigating from main page to comments page.

#### Scenario: Continue playing from main page
- **WHEN** user is listening to music on main page and navigates to comments page
- **THEN** system retrieves music state from localStorage
- **AND** if music was playing, music continues on comments page

### Requirement: Music toggle functionality
The system SHALL allow user to toggle music playback on the comments page.

#### Scenario: Toggle music on comments page
- **WHEN** user clicks the music toggle button
- **THEN** system toggles between play and pause
- **AND** system updates the button icon accordingly
- **AND** system saves state to localStorage
