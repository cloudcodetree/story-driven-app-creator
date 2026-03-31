# Dead Signal — Backlog

## Epics

### [EPIC-01] Morse Detection Engine
Core signal processing — the foundation everything else depends on.
- [x] [STORY-001] Tap input detection with adaptive timing
- [ ] [STORY-002] Audio morse detection via microphone
- [ ] [STORY-003] Visual morse detection via camera
- [ ] [SPIKE-001] Test detection accuracy in noisy environments

### [EPIC-02] Morse Transmission
Sending messages via multiple output modalities.
- [ ] [STORY-004] Text-to-morse via flashlight/screen flash
- [ ] [STORY-005] Text-to-morse via audio tones
- [ ] [STORY-006] Text-to-morse via vibration
- [ ] [STORY-007] Speech-to-text-to-morse input

### [EPIC-03] Secure Channels
Pre-arranged encrypted group communication.
- [ ] [STORY-008] Channel creation with shared key generation
- [ ] [STORY-009] Channel join flow via invite link/QR
- [ ] [STORY-010] Message encryption before morse encoding
- [ ] [STORY-011] Message decryption and verification on receive
- [ ] [SPIKE-002] Encrypted text length impact on morse transmission

### [EPIC-04] Emergency Mode
Zero-setup emergency communication for non-experts.
- [ ] [STORY-012] One-tap SOS transmission
- [ ] [STORY-013] Emergency phrase presets
- [ ] [STORY-014] Incoming SOS detection and alert

### [EPIC-05] Learning & Practice
Help users build morse proficiency over time.
- [ ] [STORY-015] Practice mode with guided lessons
- [ ] [STORY-016] Real-time feedback on tap accuracy
- [ ] [STORY-017] Speed tracking and progress history

### [EPIC-06] App Shell & UX
Core app infrastructure and user experience.
- [ ] [TASK-001] PWA setup with offline capability
- [ ] [TASK-002] Mobile-first responsive UI
- [ ] [STORY-018] Onboarding flow
- [ ] [STORY-019] Channel selection and message history

### [EPIC-07] Validation & Market Testing
Validate assumptions before building.
- [ ] [SPIKE-003] Flashlight range testing (daylight vs darkness)
- [ ] [SPIKE-004] Regulatory review of encrypted light/sound transmission
- [ ] [TASK-003] Landing page for demand validation
- [ ] [TASK-004] Community posts for interest gauging

---

**Total:** 7 Epics, 19 Stories, 4 Tasks, 4 Spikes
**MVP Scope:** EPIC-01, EPIC-02 (flashlight only), EPIC-03, EPIC-04
