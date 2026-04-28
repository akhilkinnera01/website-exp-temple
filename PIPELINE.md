# Pipeline

## Selected Build Path

Astro + GSAP ScrollTrigger + locally generated image plates + FFmpeg
video-to-scroll entry staging.

## Asset Flow

1. Source image: `ChatGPT Image Apr 27, 2026, 05_01_40 PM.png`.
2. Preservation copy: `public/temple-panorama.png`.
3. First runtime derivative: `public/temple-panorama.jpg`.
4. Sharp-generated master: `public/generated/temple-master.jpg`.
5. Sharp-generated light plates:
   - `public/generated/plate-gold.webp`
   - `public/generated/plate-bluehour.webp`
   - `public/generated/plate-stone.webp`
   - `public/generated/plate-vermilion.webp`
6. Sharp-generated depth plates:
   - `public/generated/depth-sky.webp`
   - `public/generated/depth-gopuram.webp`
   - `public/generated/depth-left-court.webp`
   - `public/generated/depth-right-horizon.webp`
   - `public/generated/depth-foreground.webp`
7. Supplied entry video: `Smooth_push-in_toward_202604280854.mp4`.
8. FFmpeg runtime derivatives:
   - `public/generated/entry-pushin.mp4`
   - `public/generated/entry-pushin-mobile.mp4`
   - `public/generated/entry-pushin-poster.jpg`
   - `public/generated/entry-pushin-poster-mobile.jpg`
   - `public/generated/entry-pushin-final.jpg`

## FFmpeg Commands

```bash
ffmpeg -y -i Smooth_push-in_toward_202604280854.mp4 -an -vf "scale=720:-2:flags=lanczos,format=yuv420p" -c:v libx264 -preset slow -crf 24 -g 8 -keyint_min 8 -sc_threshold 0 -bf 2 -movflags +faststart public/generated/entry-pushin.mp4
ffmpeg -y -i Smooth_push-in_toward_202604280854.mp4 -an -vf "scale=540:-2:flags=lanczos,format=yuv420p" -c:v libx264 -preset slow -crf 25 -g 8 -keyint_min 8 -sc_threshold 0 -bf 2 -movflags +faststart public/generated/entry-pushin-mobile.mp4
ffmpeg -y -ss 0.6 -i Smooth_push-in_toward_202604280854.mp4 -frames:v 1 -vf "scale=720:-2:flags=lanczos" -q:v 3 public/generated/entry-pushin-poster.jpg
ffmpeg -y -ss 0.6 -i Smooth_push-in_toward_202604280854.mp4 -frames:v 1 -vf "scale=540:-2:flags=lanczos" -q:v 4 public/generated/entry-pushin-poster-mobile.jpg
ffmpeg -y -sseof -0.5 -i Smooth_push-in_toward_202604280854.mp4 -frames:v 1 -vf "scale=720:-2:flags=lanczos" -q:v 3 public/generated/entry-pushin-final.jpg
```

## Motion Flow

1. Load reveal for nav, hero copy, command links, and the depth model.
2. Hero command moves to the temple entry sequence.
3. Entry section pins the viewport while GSAP maps scroll progress to a
   smoothed `requestAnimationFrame` follower for the 15-second, 360-frame
   FFmpeg-optimized video.
4. Hero background scales while the depth model rotates through scroll.
5. Depth section pins a larger 3D stage and separates image planes spatially.
6. Light-study cards reveal as a production gallery.
7. Plate controls swap the active hero light-state overlay.
8. Reduced-motion users receive static readable content with transforms disabled.

## Future Optional Expansion

The next premium step is a canvas image-sequence path for the entry video if
frame-perfect scrubbing becomes more important than the current smoother
short-GOP video `currentTime` scrub.
