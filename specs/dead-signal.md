# Dead Signal — Secure Offline Communication

## Problem Statement
When cellular infrastructure fails — during emergencies, natural disasters, large gatherings,
or in remote areas — people have no way to communicate securely using just the phone in their
pocket. Existing solutions either require dedicated hardware (Meshtastic, ham radios) or are
single-purpose morse tools that don't address real communication needs (group channels,
security, ease of use for non-experts).

## Target User
**Primary:** Emergency-conscious individuals, preppers, and outdoor enthusiasts who want a
communication fallback that requires no extra hardware. They're willing to learn basic skills
but need the app to handle the hard parts (encoding, decoding, encryption).

**Secondary:** Ham radio operators who want a digital companion for CW operations. Festival-goers
and event attendees in high-density areas where cell signal degrades.

**Tertiary (future):** Accessibility users who use morse-based input methods. STEM educators
teaching encoding and information theory.

## Value Proposition
Secure group messaging that works without cell signal, internet, or extra hardware — using
your phone's light, sound, and vibration as the transport layer.

## Market Context
- **Direct competitors**:
  - [Morse Code Engineer](https://play.google.com/store/apps/details?id=com.gyokovsolutions.morsecodeengineer) — Multi-modal morse transmit/receive, closest feature match, but no secure channels or group communication
  - [Morse Signals](https://morsesignals.com/) — Offline light/audio communication with CRC error detection, but no encryption or group support
  - [MorseCodeTranslator.ai](https://morsecodetranslator.ai/) — AI-powered web translator, not a communication tool
- **Adjacent competitors**:
  - [Meshtastic](https://meshtastic.org/) — Off-grid mesh networking, strong community, but requires dedicated LoRa hardware
  - [Briar](https://briarproject.org/) — Secure messaging via Tor/Wi-Fi/Bluetooth, but doesn't work beyond Bluetooth range without internet
- **Differentiation**: No extra hardware needed. Pre-arranged secure channels. Multi-modal (light, sound, vibration) transport. Works with just a phone.
- **Timing**: Growing interest in emergency preparedness, increasing frequency of infrastructure-disrupting events (natural disasters, grid failures), and rising awareness of communication resilience. Ham radio hardware market projected at ~$3.1B by 2033.

## Core Features (MVP)
1. **Secure channel creation** — Create a group/channel while online. Generates a shared encryption key. Members join before they need it.
2. **Text-to-morse transmission** — Type or speak a message, app encodes and transmits via flashlight, screen flash, audio tones, or vibration. User chooses modality.
3. **Multi-modal morse detection** — Decode incoming morse from audio (microphone), visual (camera), or vibration (tap patterns on phone). Adaptive to varying tempo and skill levels.
4. **Message decryption and display** — Incoming morse is decoded, verified against the channel key, and displayed as plain text.
5. **Emergency presets** — One-tap SOS and common emergency phrases, no channel required. Uses universally recognized morse patterns.

## User Journey
1. **Setup (while online):** Download app → Create a channel → Invite contacts → Everyone has shared keys stored locally. Think of it like setting up a walkie-talkie channel before a hike.
2. **Core loop (offline):** Infrastructure fails → Open app → Select channel → Type/speak message → Choose transmission mode (flash, tone, vibration) → App transmits morse. Receiver's app detects, decodes, verifies, displays as text.
3. **Retention hook:** Practice mode for learning morse. Channel history. The peace-of-mind factor — "I have a backup communication plan."

## Business Model
- **Freemium**: Free for personal use (1 channel, basic transmission/detection).
- **Premium ($4.99/mo or $29.99/yr)**: Unlimited channels, advanced detection (AI-assisted noise filtering), wearable integration, priority emergency presets, mesh relay mode (future).
- **One-time purchase option ($14.99)**: For users who dislike subscriptions. Core features unlocked permanently.
- **Enterprise/NGO licensing**: Emergency services, disaster relief organizations, event security teams. Custom pricing.

## Key Risks
| Risk | Severity | Mitigation |
|------|----------|------------|
| Morse detection accuracy in noisy environments | High | Invest heavily in signal processing. Use AI/ML for adaptive decoding. Start with controlled environments, expand. |
| Users won't set up channels before they need them | High | Onboarding that emphasizes "hope for the best, prepare for the worst." Emergency presets work without channels. |
| Limited range of phone flash/audio | Medium | Be transparent about range limitations. Position as short-to-medium range. Future: mesh relay via drone or phone chain. |
| Encryption adds complexity to morse encoding | Medium | Encryption happens at the text layer before morse encoding. Morse is just the transport — keep the layers separate. |
| Small addressable market for dedicated app | Medium | Multi-market positioning: emergency prep, ham radio companion, accessibility tool, education. Don't rely on one segment. |
| App store rejection for emergency-related claims | Low | Careful messaging — "communication tool" not "emergency device." Include disclaimers. |

## Validation Plan
**Cheapest test of the riskiest assumption (detection accuracy):**
Build a prototype that does ONE thing — detects morse code audio from a phone speaker and
translates it to text. Test it in varying noise conditions. If the detection engine can't
reliably decode morse in a moderately noisy room, the product doesn't work. This can be
validated with a weekend prototype before building anything else.

**Second validation (demand):**
Post the concept in r/amateurradio, r/preppers, r/EmergencyPreparedness, and ham radio
forums. Describe the secure channel concept. Gauge interest before building the full app.

## Recommended Next Steps
1. Build a morse audio detection prototype — test accuracy in varying noise conditions
2. Build morse visual (camera) detection — test with phone flashlight at various distances
3. If detection is viable, build the secure channel creation and key exchange flow
4. Create a landing page describing the concept, collect email signups to validate demand
5. Ship MVP with audio detection + flashlight transmission + one secure channel

## Open Questions
- What's the realistic effective range for phone flashlight morse in daylight vs. darkness?
- Should tap-detection (vibration input) use the accelerometer or require screen taps?
- How does morse encoding interact with encryption — does encrypted text become impractically long in morse?
- Is there a regulatory concern with transmitting encoded/encrypted signals via light or sound in public?
- Future: Can phones act as mesh relay nodes, receiving and retransmitting to extend range?
- Future: What drone/radio mesh integration would look like and what protocols to support
