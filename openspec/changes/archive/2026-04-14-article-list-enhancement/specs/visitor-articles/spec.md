## MODIFIED Requirements

### Requirement: Display article list
The system SHALL display a list of articles with additional information including author, like count, and comment count.

#### Scenario: Display article with author, likes, and comments
- **WHEN** user views the article list
- **THEN** each article item displays title, author nickname, like count, and comment count
- **AND** author is displayed below the title in smaller text
- **AND** like count shows heart icon with number
- **AND** comment count shows comment icon with number

#### Scenario: Display article with zero likes
- **WHEN** article has zero likes
- **THEN** like count displays "赞" without number

#### Scenario: Display article with zero comments
- **WHEN** article has zero comments
- **THEN** comment count displays "评论" without number
