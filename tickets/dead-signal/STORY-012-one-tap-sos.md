# [STORY-012] One-Tap SOS Transmission

## User Story
As a person in an emergency with no cell signal,
I want to tap a single SOS button and have my phone immediately start flashing, beeping, and vibrating the SOS pattern on repeat,
so that anyone nearby — with or without the app — can recognize I need help.

## Acceptance Criteria
- [ ] Given I open the app, when the main screen loads, then a prominent SOS button is always visible
- [ ] Given I tap SOS, when transmission starts, then all available modalities fire simultaneously (flash, screen, tone, vibration)
- [ ] Given SOS is transmitting, when the pattern completes once, then it automatically repeats
- [ ] Given SOS is repeating, when I tap "stop," then all output stops immediately
- [ ] Given my phone is locked, when SOS was started, then transmission continues (if technically possible)

## Technical Notes
- SOS pattern: ··· −−− ···  (3 dits, 3 dahs, 3 dits)
- Simultaneous output: flashlight + screen flash + audio tone + vibration
- Use wake lock API to prevent screen from sleeping during SOS
- Consider making SOS accessible from lock screen via notification (future)
- This is the most important UX in the app — must be fastest path possible

## Epic: EPIC-04 Emergency Mode
## Priority: Critical
## Points: 5
## Status: Backlog
