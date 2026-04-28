# Limitations

- The project uses the supplied image as the source for production derivatives.
  The current light states are local generated grades, not separate ChatGPT
  outputs.
- The entry uses the supplied MP4 as a video `currentTime` scrub, not a decoded
  canvas image sequence. This is lighter to ship, but not as frame-perfect as
  a full extracted-frame pipeline.
- The 3D effect is CSS 3D image staging, not a mesh-based WebGL scene.
- The legacy Vishnu SVG remains in generated assets for reference, but the
  runtime entry no longer uses the synthetic CSS door previsual.
- Asset licensing is marked as user supplied because the image was provided in
  the workspace.
- Lighthouse was not baked into the repository as an automated script. Manual
  browser checks remain part of the handoff.
