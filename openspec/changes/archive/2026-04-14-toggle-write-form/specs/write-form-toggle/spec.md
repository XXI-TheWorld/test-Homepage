## ADDED Requirements

### Requirement: Write form toggle button
The system SHALL display a "我来说两句" toggle button fixed at the bottom of the page. The button SHALL be visible at all times regardless of the form state.

#### Scenario: Display toggle button
- **WHEN** user navigates to the articles page
- **THEN** system displays a "我来说两句" button at the bottom center of the viewport
- **AND** the button is always visible

### Requirement: Toggle write form visibility
The system SHALL toggle the visibility of the write article form when the user clicks the toggle button. The form SHALL be hidden by default.

#### Scenario: Show form on button click
- **WHEN** user clicks the "我来说两句" button while the form is hidden
- **THEN** system reveals the write article form with a smooth animation
- **AND** the button text changes to "收起"

#### Scenario: Hide form on second button click
- **WHEN** user clicks the "收起" button while the form is visible
- **THEN** system hides the write article form with a smooth animation
- **AND** the button text changes back to "我来说两句"

### Requirement: Form visibility after submission
The system SHALL hide the write form after a successful article submission.

#### Scenario: Hide form after submission
- **WHEN** user successfully submits an article
- **THEN** system saves the article and hides the write form
- **AND** the form fields are cleared
- **AND** the toggle button text returns to "我来说两句"

### Requirement: Page container width
The system SHALL display the page content with a maximum width of 960px (increased from 520px).

#### Scenario: Wider container on desktop
- **WHEN** user views the page on a device with width >= 768px
- **THEN** the page container SHALL have a max-width of 960px
