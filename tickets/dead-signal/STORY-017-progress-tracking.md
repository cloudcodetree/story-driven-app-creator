# [STORY-017] Speed Tracking and Progress History

## User Story
As a user building morse proficiency,
I want to see my WPM over time and which letters I've mastered,
so that I can track my improvement and stay motivated.

## Acceptance Criteria
- [ ] Given I've practiced multiple sessions, when I view progress, then I see a WPM chart over time
- [ ] Given I've practiced letters, when I view progress, then I see which letters are mastered vs. still learning
- [ ] Given I haven't practiced in a while, when I return, then the app suggests a refresher

## Technical Notes
- Store session data: date, WPM, accuracy per letter
- Simple chart — could use Canvas or a lightweight charting lib
- "Mastered" = 90%+ accuracy over last 10 attempts

## Epic: EPIC-05 Learning & Practice
## Priority: Low
## Points: 3
## Status: Backlog
