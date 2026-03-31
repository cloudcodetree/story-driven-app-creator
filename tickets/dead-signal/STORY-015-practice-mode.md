# [STORY-015] Practice Mode with Guided Lessons

## User Story
As a user who wants to learn morse code,
I want guided lessons that teach me letters one at a time through tapping exercises,
so that I can build morse fluency at my own pace.

## Acceptance Criteria
- [ ] Given I open practice mode, when I start, then lessons begin with the simplest letters (E, T, I, A, N, M)
- [ ] Given a lesson, when a letter is shown, then I see its morse pattern and can practice tapping it
- [ ] Given I tap correctly, when the pattern matches, then positive feedback is shown and I advance
- [ ] Given I tap incorrectly, when the pattern doesn't match, then the correct pattern is shown with a hint
- [ ] Given I complete a lesson group, when I return later, then I resume where I left off

## Technical Notes
- Lesson order should follow the morse binary tree (most common letters first)
- Use spaced repetition for review of learned letters
- Progress stored in IndexedDB
- Works entirely offline

## Epic: EPIC-05 Learning & Practice
## Priority: Medium
## Points: 8
## Status: Backlog
