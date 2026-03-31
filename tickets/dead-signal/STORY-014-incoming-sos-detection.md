# [STORY-014] Incoming SOS Detection and Alert

## User Story
As a bystander with the app running,
I want the app to automatically detect incoming SOS patterns via audio or camera,
so that I'm alerted when someone nearby is signaling for help.

## Acceptance Criteria
- [ ] Given the app is in "listen" mode, when an SOS pattern is detected via audio or visual, then a loud alert is triggered
- [ ] Given an SOS is detected, when the alert fires, then the direction/source hint is shown if possible
- [ ] Given a potential SOS, when the pattern is ambiguous, then a "possible SOS detected" softer alert is shown
- [ ] Given listen mode is active, when running in the background, then detection continues (if permitted by OS)

## Technical Notes
- SOS is a well-defined pattern: ··· −−− ··· — can use pattern matching
- Only need to detect this one specific pattern for background listening
- Battery impact of continuous listening needs measurement
- Background audio detection may require native app (not PWA) — note this limitation

## Dependencies
- STORY-002 (audio detection) or STORY-003 (visual detection)

## Epic: EPIC-04 Emergency Mode
## Priority: Medium
## Points: 8
## Status: Backlog
