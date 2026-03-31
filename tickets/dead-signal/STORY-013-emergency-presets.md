# [STORY-013] Emergency Phrase Presets

## User Story
As a person in an emergency,
I want to quickly select common emergency phrases and transmit them as morse,
so that I can communicate specific needs without typing or knowing morse code.

## Acceptance Criteria
- [ ] Given I open emergency mode, when I see the preset list, then common phrases are shown (HELP, WATER, MEDICAL, FIRE, LOCATION)
- [ ] Given I tap a preset, when selected, then the morse-encoded message begins transmitting immediately
- [ ] Given I want a custom message, when I type one, then it's added to my personal presets for future use
- [ ] Given presets are available, when offline, then all presets work without any network connection

## Technical Notes
- Pre-encode common phrases as morse patterns for instant transmission
- Allow users to add custom presets
- Store presets in IndexedDB
- Consider multilingual presets (future)

## Epic: EPIC-04 Emergency Mode
## Priority: High
## Points: 3
## Status: Backlog
