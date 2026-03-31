# [STORY-002] Audio Morse Detection via Microphone

## User Story
As a user receiving a morse code transmission,
I want my phone to listen through the microphone and decode morse tones into text,
so that I can receive messages without knowing morse code myself.

## Acceptance Criteria
- [ ] Given morse code is being played as audio tones, when I open the app and start listening, then the app detects the tone frequency
- [ ] Given varying background noise, when morse tones are present, then the app filters noise and isolates the signal
- [ ] Given the sender is tapping at their own speed, when the app detects the pattern, then it adapts to the sender's tempo
- [ ] Given a complete letter pattern is detected, when followed by a pause, then the letter is decoded and displayed
- [ ] Given the audio source stops, when detection ends, then the full decoded message is shown

## Technical Notes
- Use Web Audio API for microphone access and frequency analysis
- Goertzel algorithm or FFT for tone detection at target frequency
- Need configurable target frequency (default: 700Hz, standard CW tone)
- Signal-to-noise ratio is the critical challenge — this is the riskiest feature
- Consider using a bandpass filter before classification
- Adaptive threshold for "tone on" vs "tone off" based on ambient noise floor

## Dependencies
- SPIKE-001 results should inform noise tolerance approach

## Epic: EPIC-01 Morse Detection Engine
## Priority: Critical
## Points: 13
## Status: Backlog
