## ADDED Requirements

### Requirement: Circular avatar display
The system SHALL display a profile avatar image in a circular format using CSS border-radius styling.

#### Scenario: Avatar displays as perfect circle
- **WHEN** the avatar image element is rendered in the browser
- **THEN** the image SHALL appear as a perfect circle using `border-radius: 50%`

#### Scenario: Avatar has consistent sizing
- **WHEN** the avatar image is displayed
- **THEN** it SHALL have consistent dimensions of 120px width and 120px height

#### Scenario: Avatar uses portable image path
- **WHEN** the avatar image source is specified
- **THEN** it SHALL use relative path `./images/touxiang.jpg` for portability across machines
