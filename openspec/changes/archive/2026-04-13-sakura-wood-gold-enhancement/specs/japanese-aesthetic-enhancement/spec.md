## ADDED Requirements

### Requirement: Larger sakura petals
The system SHALL display sakura petals with sizes ranging from 20px to 35px in diameter, larger than the previous 8-15px range, to create more prominent visual impact.

#### Scenario: Large petals fall continuously
- **WHEN** the page loads
- **THEN** sakura petals SHALL have sizes between 20-35px
- **AND** petal sizes SHALL be randomly distributed within this range for natural variation

### Requirement: Wood-grain button borders
The link buttons SHALL have wood-grain textured borders created using CSS gradient techniques.

#### Scenario: Wood-grain border display
- **WHEN** the page renders link buttons
- **THEN** each button SHALL display a wood-grain border effect
- **AND** the border SHALL be 2px wide
- **AND** the wood colors SHALL include shades of brown (#6B5344, #8B7355, #A08060)

### Requirement: Golden avatar border
The avatar SHALL have a golden border reminiscent of Japanese samurai helmet decorations.

#### Scenario: Golden border on avatar
- **WHEN** the avatar is rendered
- **THEN** it SHALL have a 3px solid golden border (#D4AF37)
- **AND** the border SHALL be a simple solid line (not gradient or double-line)

## MODIFIED Requirements

### Requirement: Sakura petal animation
The system SHALL continue to display falling sakura petals with the same animation behavior as before, but with increased petal size.

#### Scenario: Petals maintain animation behavior
- **WHEN** the page loads
- **AND** sakura petals are generated
- **THEN** petals SHALL fall at the same speed and sway pattern as before
- **AND** petals SHALL be sized between 20-35px instead of 8-15px
- **AND** the total petal count SHALL remain at 15-18 petals

### Requirement: Minimalist link buttons
The link buttons SHALL maintain their minimalist style but with enhanced wood-grain borders.

#### Scenario: Button hover state with wood-grain border
- **WHEN** user hovers over a link button
- **THEN** background changes to #F5F5F5
- **AND** the wood-grain border SHALL remain visible
- **AND** no animation or transition effects are applied
