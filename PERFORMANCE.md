# PERFORMANCE BUDGET: Varun Estates

## Goal: Cinematic Showcase
- **LCP Target:** < 2.5s on Fast 4G / 5G.
- **Assets:** High-resolution assets (4MB+ acceptable), but all imagery must be aggressively compressed to WebP or AVIF using Astro's Image component.
- **Blocking:** No heavy JavaScript blocks the main thread. GSAP ScrollTrigger is deferred/lazy-loaded and runs primarily on composited layers (opacity, transform).
- **Fonts:** All Google Fonts are preconnected to minimize FOUT (Flash of Unstyled Text).