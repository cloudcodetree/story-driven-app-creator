# [STORY-004] Text-to-Morse via Flashlight/Screen Flash

## User Story
As a user who needs to send a message without cell signal,
I want to type a message and have my phone's flashlight or screen flash it in morse code,
so that someone nearby (with or without the app) can see and decode it.

## Acceptance Criteria
- [ ] Given I type a text message, when I tap "transmit," then the app encodes it to morse
- [ ] Given I choose "flashlight" mode, when transmitting, then the phone's rear flashlight flashes the morse pattern
- [ ] Given I choose "screen" mode, when transmitting, then the screen flashes white/black for the morse pattern
- [ ] Given the transmission is in progress, when I tap "stop," then transmission stops immediately
- [ ] Given any message, when transmitting, then the current character and progress are shown on screen
- [ ] Given the user's WPM setting, when transmitting, then the timing matches the selected speed

## Technical Notes
- Use Torch API (mediaDevices.getUserMedia with torch constraint) for flashlight control
- Screen flash is simpler — toggle background color via CSS
- Timing must match standard morse ratios: dit=1, dah=3, element gap=1, letter gap=3, word gap=7
- Configurable WPM (5-25 range, default 10 for readability)
- Show a preview of the morse pattern before transmitting

## Epic: EPIC-02 Morse Transmission
## Priority: Critical
## Points: 5
## Status: Backlog
