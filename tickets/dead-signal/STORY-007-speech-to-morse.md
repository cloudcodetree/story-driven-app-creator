# [STORY-007] Speech-to-Text-to-Morse Input

## User Story
As a user in an emergency who can't type,
I want to speak a message and have the app convert my speech to text and then to morse,
so that I can transmit without needing to interact with the screen.

## Acceptance Criteria
- [ ] Given I tap the microphone button, when I speak clearly, then my speech is transcribed to text
- [ ] Given the transcription is shown, when I confirm it, then it's encoded and ready to transmit
- [ ] Given poor speech recognition, when the transcription is wrong, then I can edit it before transmitting
- [ ] Given no internet connection, when I try speech input, then the app uses on-device speech recognition if available, or shows a clear error

## Technical Notes
- Use Web Speech API (SpeechRecognition)
- On-device recognition available in Chrome/Edge — works offline
- Safari support is limited — need fallback
- This is a convenience feature, not core — text input is the primary method

## Epic: EPIC-02 Morse Transmission
## Priority: Low
## Points: 3
## Status: Backlog
