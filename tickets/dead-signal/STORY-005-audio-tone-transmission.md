# [STORY-005] Text-to-Morse via Audio Tones

## User Story
As a user who needs to send a message via sound,
I want to type a message and have my phone emit morse code as audio tones,
so that someone nearby with the app can detect and decode it.

## Acceptance Criteria
- [ ] Given I type a text message, when I choose "audio" and tap "transmit," then the phone plays morse tones
- [ ] Given the app is transmitting, when a dit is played, then a short tone sounds at the configured frequency
- [ ] Given the app is transmitting, when a dah is played, then a long tone sounds (3× dit duration)
- [ ] Given the user's volume is set, when transmitting, then the tone is audible at the phone's current volume
- [ ] Given I tap "stop," when transmission is active, then audio stops immediately

## Technical Notes
- Use Web Audio API OscillatorNode for tone generation
- Default frequency: 700Hz (standard CW tone, cuts through noise well)
- Configurable frequency for advanced users
- Smooth envelope (attack/release) to avoid clicks/pops
- Works offline — no network needed for audio generation

## Epic: EPIC-02 Morse Transmission
## Priority: High
## Points: 3
## Status: Backlog
