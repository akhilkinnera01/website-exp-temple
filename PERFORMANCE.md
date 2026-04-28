# Performance

## Current Choices

- Astro static output.
- Main hero derivative is `public/generated/temple-master.jpg` at 220 KB.
- Light-state plates are WebP derivatives between 128 KB and 198 KB.
- Depth plates are WebP derivatives between 35 KB and 79 KB.
- Supplied entry video is preserved at about 12 MB.
- Runtime desktop entry video is `public/generated/entry-pushin.mp4`, H.264,
  no audio, fast-start, 720x1280, 15s, 360 frames, short GOP for smoother
  scroll seeking.
- Runtime mobile entry video is `public/generated/entry-pushin-mobile.mp4`,
  H.264, no audio, fast-start, 540x960, short GOP.
- Poster, mobile poster, and final-frame JPGs are local FFmpeg derivatives.
- PNG source is preserved but not the primary browser asset.
- No WebGL or remote font loading.
- CSS uses fixed breakpoint typography, not viewport font scaling.

## Verification Target

- `npm run build` must pass.
- Browser console must be free of runtime errors.
- Mobile viewport must keep text legible and controls reachable.

## Known Tradeoff

The entry video is now the heaviest runtime asset. The short-keyframe encode is
larger than the first compression pass, but it makes scroll seeking feel less
like broken still frames. Mobile receives a smaller 540px-wide video source.
