## ADDED Requirements

### Requirement: Like an article
The system SHALL allow visitors to like an article. Each visitor (identified by nickname) can only like an article once.

#### Scenario: Like an article
- **WHEN** visitor clicks the like button on an article
- **THEN** system adds the visitor's nickname to the article's likes array
- **AND** system updates the like count display
- **AND** system changes the like button to filled state

#### Scenario: Unlike an article
- **WHEN** visitor clicks the like button again on an article they have already liked
- **THEN** system removes the visitor's nickname from the article's likes array
- **AND** system updates the like count display
- **AND** system changes the like button to outline state

#### Scenario: Like button display
- **WHEN** visitor has already liked an article
- **THEN** the like button SHALL display in filled/red state
- **WHEN** visitor has not liked an article
- **THEN** the like button SHALL display in outline/gray state

### Requirement: Like a comment
The system SHALL allow visitors to like a comment. Each visitor can only like a comment once.

#### Scenario: Like a comment
- **WHEN** visitor clicks the like button on a comment
- **THEN** system adds the visitor's nickname to the comment's likes array
- **AND** system updates the like count display

#### Scenario: Unlike a comment
- **WHEN** visitor clicks the like button again on a comment they have already liked
- **THEN** system removes the visitor's nickname from the comment's likes array
- **AND** system updates the like count display

### Requirement: Like count display
The system SHALL display the number of likes for each article and comment.

#### Scenario: Display like count
- **WHEN** visitor views an article or comment
- **THEN** system displays the number of likes next to the like button
- **AND** if like count is 0, display "赞" without a number
