## ADDED Requirements

### Requirement: White background minimalist design
The system SHALL display the LinkPage with a pure white (#FFFFFF) background to create a clean, serene visual environment reminiscent of Japanese shrine architecture.

### Requirement: Sans-serif typography
The system SHALL use Noto Sans JP as the primary font family, with font weights 300 (light) for secondary text and 400 (regular) for primary text, to achieve a minimalist aesthetic.

### Requirement: Generous spacing
The system SHALL use a spacing system that creates vertical rhythm and breathing room:
- Page padding: 48px (desktop), 24px (mobile)
- Container max-width: 480px
- Element gap between header and links: 32px
- Gap between buttons: 12px
- Button height: 52px

### Requirement: Simplified visual elements
The system SHALL NOT display any glow effects, shadows, or decorative borders. The avatar SHALL have only a subtle light gray border (#E0E0E0) with no shadow or glow.

### Requirement: Minimalist link buttons
The link buttons SHALL have the following styling:
- Background: pure white (#FFFFFF)
- Border: 1px solid #E0E0E0
- No border-radius (sharp corners evoke shrine torii aesthetic)
- Text color: #1A1A1A
- Font: Noto Sans JP, weight 400

#### Scenario: Button hover state
- **WHEN** user hovers over a link button
- **THEN** background changes to #F5F5F5 and text color remains #1A1A1A
- **AND** no animation or transition effects are applied

### Requirement: Sakura petal animation
The system SHALL display falling sakura (cherry blossom) petals across the page for ambient decoration.

#### Scenario: Petals fall continuously
- **WHEN** the page loads
- **THEN** 15-20 sakura petals SHALL be visible falling simultaneously
- **AND** petals SHALL have varying fall durations between 8-15 seconds
- **AND** petals SHALL sway horizontally using a sine wave pattern to simulate wind
- **AND** petals SHALL be colored rgba(255, 182, 193, 0.6) (translucent pink)
- **AND** petal sizes SHALL vary between 8-15px

#### Scenario: Petals do not obstruct interaction
- **WHEN** sakura petals are falling
- **THEN** petals SHALL have pointer-events: none
- **AND** petals SHALL be positioned below all interactive content in z-index
