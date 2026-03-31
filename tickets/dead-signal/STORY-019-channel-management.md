# [STORY-019] Channel Selection and Message History

## User Story
As a user with multiple channels,
I want to select a channel and see past messages sent and received on it,
so that I can keep track of communications and switch between groups.

## Acceptance Criteria
- [ ] Given I have channels, when I open the channels tab, then I see a list of all channels with last activity
- [ ] Given I select a channel, when it opens, then I see a chronological message history
- [ ] Given messages exist, when I view them, then each shows: sender indicator, timestamp, plaintext, and transmission mode used
- [ ] Given I want to transmit, when I'm on a channel, then the transmit UI is pre-configured for that channel's key

## Technical Notes
- Messages stored in IndexedDB, keyed by channel
- Sender identification is limited — morse doesn't carry identity metadata
- Consider adding a short callsign prefix to messages for sender identification
- Message history should be lightweight — these are short morse messages, not chat logs

## Dependencies
- STORY-008 (channels must exist)

## Epic: EPIC-06 App Shell & UX
## Priority: Medium
## Points: 5
## Status: Backlog
