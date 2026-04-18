# PIPELINE PLAN: Varun Estates

## Pipeline A: Nano Banana 2 (Imagery)
- **Purpose:** Used for the signature moment hero still, background textures (like subtle topographical lines or sunbaked earth), and high-quality photography placeholders.
- **Workflow:** Generate prompts in `PROMPTS.md`. Akhil will run these through Gemini 3.1 Flash Image (Nano Banana 2) and save the outputs as high-res WebP/JPEGs.
- **Optimization:** We will convert these images to WebP/AVIF and optimize them aggressively using Astro's native `<Image>` component to maintain the 4MB+ performance budget without hurting LCP.

## Pipeline E: GSAP ScrollTrigger & CSS Scroll-Driven Motion (Motion)
- **Purpose:** To choreograph the unhurried, editorial scroll fades and the signature hero moment transformation (typography fading, background slight scale/blur).
- **Workflow:** 
  - GSAP will handle complex timelines, like the hero element's staggered text reveal and the background image's slow parallax zoom.
  - Native CSS scroll-driven animations will be used for lightweight secondary elements to keep the main thread unblocked.