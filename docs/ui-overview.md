# DJ Engine — UI / UX Integration Overview

This document describes how DJ Engine integrates into a modern
music streaming application UI without increasing user complexity.

The UI patterns described here are platform-neutral and based on
common interaction models used in large-scale music streaming services
(e.g. YouTube Music and similar platforms), referenced for illustrative purposes only.

---

## Design Principles

- DJ Engine extends existing playback UI rather than replacing it
- Complexity is revealed progressively as the user advances
- No DJ knowledge is required in AI and Assist modes
- Manual control remains fully available for advanced users

---

## Entry Point

DJ Engine is activated from the standard **Now Playing** screen.

- A new **DJ** button is placed near Shuffle / Repeat controls
- First activation shows a one-line explanation:

> “DJ Engine mixes tracks in real time instead of switching them.”

This explanation is shown only once.

---

## Mode Selection

After activation, the user selects one of three modes:

- **Manual DJ** — Full control, user mixes
- **Assist DJ** — System assists, user confirms
- **AI DJ** — Fully automatic mixing

The selected mode is remembered and can be changed at any time.

---

## AI DJ Mode (Mass Audience)

AI DJ mode is designed for listeners who want a continuous music experience
without manual interaction.

UI characteristics:

- Standard playback screen remains unchanged
- Additional controls:
  - **Energy slider** (Low ↔ High)
  - **Vibe selector** (Chill / Drive / Night / Focus)
- Status indicator:
  > “Next mix in 8 bars”

No deck controls or track selection are exposed in this mode.

---

## Assist DJ Mode

Assist DJ mode provides guided control for non-professional DJs.

UI characteristics:

- Simplified two-deck view
- **Deck A**: Master output
- **Deck B**: Cue (headphones)
- System analyzes BPM and phrasing
- Optimal mix timing is suggested visually
- User confirms transition via **MIX NOW**

The system never initiates a transition without confirmation.

---

## Manual DJ Mode

Manual DJ mode exposes full DJ-style controls.

UI characteristics:

- Compact DJ mixer layout
- Two decks
- Crossfader
- Cue / Master mix control
- EQ (Low / Mid / High)
- Optional sync assistance

No automation prompts are shown in this mode.

---

## Cross-Platform Behavior

| Platform | Supported Modes |
|--------|-----------------|
| Mobile | Manual / Assist / AI |
| Web | Assist / AI |
| TV | AI only |
| Car | AI + Energy control |

DJ Engine adapts to platform constraints while preserving
a consistent conceptual model.

---

## Progressive User Journey

DJ Engine supports natural user progression:

- Listener → AI DJ
- Interested user → Assist DJ
- Advanced user → Manual DJ

This progression occurs without switching applications or tools.
