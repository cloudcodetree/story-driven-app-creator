# [STORY-006] Text-to-Morse via Vibration

## User Story
As a user who needs to send a silent morse message,
I want to type a message and have my phone vibrate the morse pattern,
so that someone holding the phone or wearing a connected wearable can feel and decode it.

## Acceptance Criteria
- [ ] Given I type a text message, when I choose "vibration" and tap "transmit," then the phone vibrates the morse pattern
- [ ] Given a dit, when vibrating, then a short vibration pulse is felt
- [ ] Given a dah, when vibrating, then a longer vibration pulse is felt (3× dit)
- [ ] Given the pattern completes, when the message is done, then vibration stops
- [ ] Given I tap "stop," when vibrating, then vibration stops immediately

## Technical Notes
- Use navigator.vibrate() API with pattern arrays
- Pattern format: [vibrate, pause, vibrate, pause, ...]
- Pre-compute the full vibration pattern array from the morse encoding
- Note: vibrate API support varies — not available on iOS Safari
- Wearable forwarding via notification vibration (future enhancement)

## Epic: EPIC-02 Morse Transmission
## Priority: Medium
## Points: 3
## Status: Backlog
