## ADDED Requirements

### Requirement: Announcement sidebar item is visually distinct
The system SHALL display 公告 at the top of the sidebar with red styling.

#### Scenario: Announcement styled in red
- **WHEN** user views comments.html
- **THEN** 公告 appears first in the sidebar
- **AND** 公告 has red background/text color

#### Scenario: Non-admin cannot see announcement filter
- **WHEN** user is not logged in as admin
- **THEN** 公告 is not visible in the sidebar

### Requirement: Latest announcement is pinned permanently
The system SHALL display the most recent 公告 article at the top of the article list permanently.

#### Scenario: Pinned announcement displayed
- **WHEN** there exists at least one 公告 article
- **THEN** the most recent 公告 article is displayed at the top with "置顶" label
- **AND** it remains visible regardless of category filter

#### Scenario: No announcement exists
- **WHEN** there are no 公告 articles
- **THEN** no pinned item is displayed

#### Scenario: Pinned announcement has distinct styling
- **WHEN** announcement is pinned
- **THEN** it has distinct visual styling (different border, "置顶" badge)
