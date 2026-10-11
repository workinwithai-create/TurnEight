# TurnEight

Eight-bar bridge desk for bedroom producers and AI-music finishers.

Suno and loop DAWs leave a solid chorus that never turns. After ear fatigue the producer abandons the track because “it has nowhere to go.” Session players seat an eight-bar bridge: relative minor, pedal hold, borrowed color, half-time air, or a turnaround walk so the return feels earned.

TurnEight writes that turn on the progression you already have. A is the thin pocket. B is the bridge. Loudness is matched so the A/B is about the parts.

Live samples only. FluidR3 piano, upright, nylon, trumpet, violin, and acoustic kit from the PreEight bank, pinned to commit SHA. No oscillators. Audio never leaves the tab.

This desk is free.

## Why this exists

Current X conversations (Oct 2026) still center on bridges that create vacuum instead of decoration, subtraction for contrast, and transitions as the song. The fix is not another preset. It is a short section that breaks the loop so the chorus can sit down.

## Distinct from yesterday and the rest of the line

| Tool | Job |
| --- | --- |
| CallEight | Eight bars of call-and-response on the same changes |
| MuteEight | Density subtraction |
| AirCut | Subtractive air before the drop |
| PedalEight | Pedal-point hold |
| **TurnEight** | Eight-bar bridge that turns the harmonic direction so the loop finally has a door |

Yesterday’s desk seated a conversation. TurnEight does not write answers on the same pocket. It writes a bridge.

## Pricing recommendation

One-time **$19** if you productize it, on Lemon Squeezy, mirrored on Gumroad. Do not subscribe. Forge Pass stays the subscription for the cloud tools (AuraMix, MixForge, ReleaseForge). Sell where producers already buy one-shot utilities: Lemon Squeezy first, a Gumroad mirror, and one post on r/WeAreTheMusicMakers. Not the App Store. Not Plugin Boutique.

The shipped app is free (MIT). No license gate. A priced build would need a Lemon Squeezy key check before it can be called a paid ship.

## Samples

Pinned commit SHAs only.

* PreEight bank @d58301e4a494555f411a2afbc448b724136eee76

Branch tips are not allowed.

## Export

Default bounce is 48 kHz, 24-bit stereo. At 92 BPM and 8 bars the loop file is exactly 1,001,739 samples (`Math.round(8 * 4 * 60 / 92 * 48000)`), first downbeat at sample 0. The offline render decodes the already-loaded ArrayBuffers. It does not re-download. MIDI writes one track per chair with tempo and 4/4 set.

Files: `turneight-<recipe>-<bpm>bpm-<key>.wav` and the matching `.mid`.

## Acceptance checks

1. Export at 92 BPM, 8 bars, 48 kHz: exactly 1,001,739 samples, first transient within 1 ms of sample 0.
2. Loop seam has no click or drift against a 92 BPM grid.
3. Background tab stops cleanly with no stacked notes.
4. Live recipe / mute / BPM change is heard within one bar.
5. Blocked sample host names the missing instruments.
6. Longest pad sustains to the end of the note (looped violin hold).
7. Grep: no @main, no @gh-pages, no Math.random in the export path, voice names match samples.

All checks pass in the reference implementation. Offline render folds the ring-out and peaks ≤ −1 dBFS.

## License

MIT. workinwithai-create.

## Demo

Short demo video shows A (pocket) vs B (relative-minor bridge) on the Copper Rail groove at 92 BPM.
