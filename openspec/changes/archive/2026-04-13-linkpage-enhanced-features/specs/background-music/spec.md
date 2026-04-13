## ADDED Requirements

### Requirement: Background music control
The system SHALL provide a music playback control button that allows users to play or pause background music.

#### Scenario: Music starts muted
- **WHEN** the page loads
- **THEN** the background music SHALL be loaded
- **AND** the music SHALL start in muted state

#### Scenario: Toggle play/pause
- **WHEN** user clicks the music control button while music is paused
- **THEN** the music SHALL start playing unmuted
- **AND** the button icon SHALL change to pause icon

#### Scenario: Pause music
- **WHEN** user clicks the music control button while music is playing
- **THEN** the music SHALL pause
- **AND** the button icon SHALL change to play icon
