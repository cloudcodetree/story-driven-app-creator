# [STORY-001] Tap Input Detection with Adaptive Timing

## User Story
As a user learning morse code,
I want to tap short and long presses on a button and see them decoded into text in real-time,
so that I can communicate via morse without memorizing the full alphabet.

## Acceptance Criteria
- [x] Given I hold the button briefly, when I release, then a dit (·) is registered
- [x] Given I hold the button longer, when I release, then a dah (−) is registered
- [x] Given I tap at any speed, when I've tapped a few times, then the system calibrates to my tempo
- [x] Given I pause between characters, when the gap exceeds 3× dit duration, then the current buffer commits as a letter
- [x] Given I pause longer, when the gap exceeds 7× dit duration, then a word space is inserted
- [x] Given the decoded buffer matches a morse pattern, when committed, then the correct letter is displayed
- [x] Given the decoded buffer doesn't match, when committed, then a ? is shown

## Technical Notes
- Adaptive threshold uses two sliding window arrays (ditDurations[], dahDurations[], max 20 each)
- Threshold = midpoint of average dit and average dah
- Initial threshold: 200ms until calibrated (needs 2+ dits and 1+ dah)
- Uses performance.now() for sub-millisecond timing accuracy
- Vibration feedback via navigator.vibrate API

## Epic: EPIC-01 Morse Detection Engine
## Priority: Critical
## Points: 5
## Status: Done
