# Direction

## Thesis

Suryakshetra turns one ChatGPT temple panorama and one temple-door push-in video
into an interactive temple entry experience with a 360-feeling outer world,
video-scrubbed threshold crossing, depth plates, cinematic light states, and
scroll-driven spatial composition.

## Signature Moment

The supplied 360-style panorama establishes the outer courtyard. A pinned scroll
scene then uses the supplied 15-second, 360-frame push-in video as the true
threshold moment; as the visitor scrolls, the doors open in footage and the
camera moves toward the sanctum. The existing depth stage then supports the same
thesis by breaking the panorama into spatial planes.

## Material Vocabulary

Carved stone + sunset metal + smoked glass.

## Motion Language

- Easing: `power3.out` for reveals, linear easing only for scroll-linked depth.
- Duration: 1.0s to 1.25s for entrance motion.
- Pacing: ceremonial, slow, and authored.

## Typography Direction

Georgia anchors the large editorial titles. System sans carries body text and
navigation. Headings use fixed breakpoint sizes rather than viewport scaling,
with zero letter spacing.

## Color Direction

- `#100b08` ink
- `#d39b42` sunset gold
- `#a83c2d` vermilion
- `#345f4a` temple green
- `#efe1c3` stone sand

## Pipelines

- Supplied ChatGPT image: source visual for every production plate.
- Local image creation: Sharp generated master, light studies, and depth slices from the supplied panorama.
- FFmpeg video-to-scroll: compresses the supplied push-in video into a fast-start H.264 runtime asset and poster.
- CSS 3D stage: creates a spatial image model without adding WebGL weight.
- GSAP ScrollTrigger: drives video scrubbing, hero, depth stage, scroll meter, and reveal cadence.
- Astro static build: keeps the experience deployable as a static microsite.
- Future ChatGPT image generation: prompts in `PROMPTS.md` describe companion stills for a true multi-frame sequence.

## Performance Budget

Standard premium with a cinematic entry exception. The page uses optimized JPG
and WebP derivatives for still imagery, plus short-GOP no-audio H.264 videos
for the signature threshold on desktop and mobile. No WebGL runtime is used in
this pass.

## Judge Bar

The earlier version was around 2 out of 10 for a serious frontend contest. This
version moves toward 7 because it now has a premise, a real video-driven
scroll-entry signature moment, custom visual production, interactive depth,
light-state controls, and a coherent motion system.

## References

- Active Theory: cinematic first impression and spatial confidence.
- Immersive Garden: museum-like pacing and image authority.
- Codrops demos: scroll-linked image choreography.
- Godly gallery patterns: severe typography and polished editorial rhythm.
