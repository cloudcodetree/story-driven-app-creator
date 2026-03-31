# [STORY-011] Message Decryption and Verification on Receive

## User Story
As a channel member receiving an encrypted morse message,
I want the app to decode the morse, decrypt the text, and verify it came from my channel,
so that I can read the message and trust its authenticity.

## Acceptance Criteria
- [ ] Given encrypted morse is detected, when fully decoded, then the app attempts decryption with all active channel keys
- [ ] Given a matching channel key, when decryption succeeds, then the plaintext message is displayed with the channel name
- [ ] Given the HMAC verifies, when displayed, then a "verified" indicator is shown
- [ ] Given no channel key matches, when decryption fails, then the raw morse is shown with a "no matching channel" notice
- [ ] Given a corrupted or incomplete transmission, when decryption fails, then a clear error explains what went wrong

## Technical Notes
- Try decryption against all stored channel keys (should be few — fast)
- HMAC verification prevents displaying corrupted decryptions
- Show both the raw morse and decrypted text for transparency
- Error handling is critical — partial transmissions are likely in real conditions

## Dependencies
- STORY-010 (encryption format must match)
- STORY-002 or STORY-003 (need a detection modality to receive)

## Epic: EPIC-03 Secure Channels
## Priority: High
## Points: 5
## Status: Backlog
