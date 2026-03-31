# [STORY-010] Message Encryption Before Morse Encoding

## User Story
As a channel member sending a message,
I want my text message to be encrypted before it's converted to morse,
so that anyone intercepting the morse signal can't read the content.

## Acceptance Criteria
- [ ] Given I'm on a channel, when I type a message and transmit, then the text is encrypted before morse encoding
- [ ] Given encryption is applied, when the morse is transmitted, then the flashes/tones represent the encrypted text, not the plaintext
- [ ] Given no channel is selected, when I transmit, then the message is sent as unencrypted morse (plaintext mode)
- [ ] Given encryption increases message length, when transmitting, then an estimated transmission time is shown before sending

## Technical Notes
- Encrypt at text layer: plaintext → encrypt → base64 or hex → morse encode
- AES-256-GCM via Web Crypto API
- Include a short HMAC for integrity verification
- Encrypted output will be longer than plaintext — this is a real tradeoff
- Consider compression before encryption to reduce length
- SPIKE-002 should quantify the length impact

## Dependencies
- STORY-008 (need a channel with a key)
- SPIKE-002 (should inform UX around transmission time)

## Epic: EPIC-03 Secure Channels
## Priority: High
## Points: 5
## Status: Backlog
