# [STORY-008] Channel Creation with Shared Key Generation

## User Story
As a group organizer preparing for an event or trip,
I want to create a secure communication channel and generate a shared encryption key,
so that my group can communicate via morse if cell signal fails.

## Acceptance Criteria
- [ ] Given I'm online, when I tap "Create Channel," then a new channel is created with a unique name
- [ ] Given a channel is created, when it's initialized, then a symmetric encryption key is generated
- [ ] Given the key is generated, when creation completes, then the key is stored locally on-device only
- [ ] Given my channel exists, when I view it, then I see the channel name, member count, and creation date
- [ ] Given I have multiple channels, when I open the app, then I see a list of all my channels

## Technical Notes
- Use Web Crypto API for key generation (AES-256-GCM)
- Keys stored in IndexedDB, never transmitted after initial share
- Channel metadata: name, created_at, member_count, key_id
- No server needed for channel existence — it's just a local key agreement

## Epic: EPIC-03 Secure Channels
## Priority: High
## Points: 5
## Status: Backlog
