# Paint 4D — Version 1

A touch-friendly, installable 4D geometry painting web app. No account or backend needed.

## Publish using GitHub Pages

1. Create a **public** repository named `paint-4d`.
2. Upload the **contents of this folder** (not the ZIP itself) into the repository root and commit.
3. Open **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Select branch `main`, folder `/ (root)`, then **Save**.
5. Wait for the Pages link. Open it in Safari, tap Share → Add to Home Screen.

## Features

- Straight 4D line segments with branching from existing dots.
- Genuine 4D line intersection splitting (not false screen-projection crossings).
- Free eraser that cuts lines; fill tool for closed line faces.
- 32-colour palette, custom colour, adjustable line width.
- 4D tesseract, pentachoron, hypersphere visualisation (sampled 3D cross-section), custom dot-and-line geometry.
- Six independent 4D rotation planes (XY, XZ, XW, YZ, YW, ZW).
- Up to 10 layers with visibility/lock controls (double-click name to rename).
- Browser autosave, named projects, import/export `.paint4d`, PNG, SVG, JSON.
- Pan and zoom, undo and redo, offline caching after first load.

## Current limitations

- 4D drawing uses X/Y screen placement with editable Z/W values; rotated screen-to-4D picking is approximate rather than full inverse ray-casting.
- The hypersphere is rendered as a sampled 3D cross-section, not a full 4D surface mesh.
- The fill tool detects closed faces in the screen projection; complex overlapping 4D geometry may need more advanced topology handling.
- Erasing a stroke clears its existing fills in that layer; re-fill the resulting closed shapes.
- Autosave uses browser localStorage, which can be cleared by Safari; export `.paint4d` backups.
- The SVG icon works in modern browsers, but iPad Home Screen icons may need a PNG apple-touch-icon for optimal appearance.

All geometry is represented with four-dimensional coordinates; this is a real geometry prototype, not a 4D-looking picture editor.
