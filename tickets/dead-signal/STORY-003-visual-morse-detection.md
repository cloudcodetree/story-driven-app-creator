# [STORY-003] Visual Morse Detection via Camera

## User Story
As a user receiving a morse code light signal,
I want my phone's camera to detect flashing light patterns and decode them into text,
so that I can receive messages transmitted via flashlight or screen flash.

## Acceptance Criteria
- [ ] Given a flashlight is flashing morse patterns, when I point my camera at it, then the app detects brightness changes
- [ ] Given varying ambient lighting, when morse flashes are present, then the app distinguishes signal from background
- [ ] Given the sender is flashing at their own speed, when the app detects the pattern, then it adapts to the sender's tempo
- [ ] Given distance reduces flash brightness, when the signal is still detectable, then decoding still works
- [ ] Given a complete letter pattern is detected, when followed by a dark pause, then the letter is decoded and displayed

## Technical Notes
- Use getUserMedia for camera access, sample a region of the video feed
- Track average brightness of center region frame-by-frame
- Threshold brightness changes to detect "on" vs "off" state
- Same adaptive timing logic as STORY-001 but applied to brightness duration
- Frame rate limits detection speed (~30fps = ~33ms minimum resolution)
- Consider letting user tap a "calibrate" region to identify the light source location

## Dependencies
- SPIKE-003 results should inform effective range expectations

## Epic: EPIC-01 Morse Detection Engine
## Priority: High
## Points: 13
## Status: Backlog
