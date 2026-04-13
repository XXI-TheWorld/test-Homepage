## ADDED Requirements

### Requirement: Dark mode toggle
The system SHALL provide a toggle button in the top-right corner that allows users to switch between light and dark themes.

#### Scenario: Toggle from light to dark
- **WHEN** user clicks the theme toggle button while in light mode
- **THEN** the theme SHALL change to dark mode
- **AND** the transition SHALL be smooth with a 0.3s animation

#### Scenario: Toggle from dark to light
- **WHEN** user clicks the theme toggle button while in dark mode
- **THEN** the theme SHALL change to light mode
- **AND** the transition SHALL be smooth with a 0.3s animation

### Requirement: Theme persistence
The system SHALL remember the user's theme preference using localStorage.

#### Scenario: Theme preference saved
- **WHEN** user toggles the theme
- **THEN** the current theme SHALL be saved to localStorage
- **AND** on page reload, the saved theme SHALL be restored
