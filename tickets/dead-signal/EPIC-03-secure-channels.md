# [EPIC-03] Secure Channels

## Description
Pre-arranged encrypted communication channels. Users create a group while online, generating
a shared secret key. When infrastructure fails, they communicate via morse with messages
encrypted at the text layer before encoding.

## Goal
Enable two or more users to communicate securely via morse, with messages that can't be
read by anyone who intercepts the signal without the shared key.

## Stories
- [ ] [STORY-008] Channel creation with shared key generation
- [ ] [STORY-009] Channel join flow via invite link/QR
- [ ] [STORY-010] Message encryption before morse encoding
- [ ] [STORY-011] Message decryption and verification on receive
- [ ] [SPIKE-002] Encrypted text length impact on morse transmission

## Priority: High
## Status: Backlog
