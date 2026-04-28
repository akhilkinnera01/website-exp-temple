# Motion

## Principle

The page has one signature gesture: the visitor scrolls through the supplied
temple-door push-in video, then the panorama splits into a spatial temple model
and recomposes into cinematic light studies.

## Rules

- Large text enters once with `power3.out`.
- Scroll-linked movement uses linear easing and stays slow.
- Entry scroll progress maps to the 15-second, 360-frame video through a
  smoothed animation-frame follower.
- The video grade should feel like approach and glow, not a jump scare.
- The old CSS lamps, smoke, and synthetic doors stay removed from the runtime.
- Depth plates rotate with scroll and respond gently to pointer position.
- Supporting sections reveal upward by a small distance only.
- Plate controls swap light state without changing layout.
- Marker labels appear on hover, focus, or click.
- `prefers-reduced-motion` disables choreography and keeps content readable.

## Values

- Entrance duration: 1.0s to 1.25s.
- Reveal offset: 42px to 44px.
- Hero scale range: 1.02 to 1.08.
- Entry video scrub range: 0.00s to 14.98s.
- Entry scroll scrub smoothing: 0.65s GSAP scrub plus frame-level time easing.
- Entry atmosphere scale range: 1.00 to 1.05.
- Depth model rotation range: around 16 to 18 degrees on scroll.
- Observatory scale range: 1.00 to 1.08.
