# [STORY-009] Channel Join Flow via Invite Link/QR

## User Story
As a group member invited to a secure channel,
I want to join by scanning a QR code or tapping an invite link,
so that I have the shared key stored on my device before I need it.

## Acceptance Criteria
- [ ] Given I receive a QR code, when I scan it with the app, then the channel key is imported to my device
- [ ] Given I receive an invite link, when I tap it, then the app opens and imports the channel key
- [ ] Given I've joined a channel, when I view my channels, then the new channel appears in my list
- [ ] Given the invite contains the key, when imported, then no further network calls are needed
- [ ] Given someone tries to join with an expired/invalid invite, when they scan it, then a clear error is shown

## Technical Notes
- QR code contains: channel name + base64-encoded key (or key derivation material)
- Invite link uses URL fragment (#) so key never hits a server
- Consider time-limited invites for security
- QR generation: use a lightweight QR library (qrcode.js or similar)
- Camera scanning: use native BarcodeDetector API or jsQR library

## Dependencies
- STORY-008 (channel must exist before invites work)

## Epic: EPIC-03 Secure Channels
## Priority: High
## Points: 5
## Status: Backlog
