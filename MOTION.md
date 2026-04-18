# MOTION CHOREOGRAPHY: Varun Estates

## Core Rules
- **Easing:** `power2.inOut` for initial loads, `none` (linear) for scroll-scrubbed moments, `power2.out` for reveals.
- **Respect:** All animations must respect `prefers-reduced-motion` at the CSS layer or GSAP timeline level.

## Sequence 1: The Initial Reveal (Hero)
1. **Logo:** Fades in over 1.5s.
2. **Typography (Bilingual):** Staggers in from below (y: 12) with `power3.out`. Telugu script lags slightly behind English for an elegant dual-reading rhythm.
3. **Subtext:** Fades in softly beneath.

## Sequence 2: The Signature Moment (Scroll Scrub)
1. **Background:** Scales slowly from 1.0 to 1.15 while its opacity dims to 0.3 to push the land "back" and pull the user "forward".
2. **Typography:** Translates up (y: -50) and fades out at the exact rate of the user's scroll.