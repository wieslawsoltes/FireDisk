# FireDisk

FireDisk is a zero-dependency disk space analyzer with interactive SVG flame graphs.
It runs entirely in the browser and supports macOS, Windows, and Linux.

## Features
- File System Access API scanning with folder upload fallback
- Interactive flame and radial layouts with zoom, breadcrumbs, and search
- Side panel preview with live hover details and largest items
- Tiny-item grouping, depth limits, and dotfile toggles
- Pure HTML/CSS/JS, no external dependencies

## Getting Started
Open `index.html` in a modern browser.

For the best experience, use a Chromium-based browser (Chrome, Edge, Arc) so the
native directory picker is available. Firefox and Safari will fall back to
folder upload.

If the directory picker fails to open from `file://`, serve the file locally:

```sh
python -m http.server
```

Then visit `http://localhost:8000`.

## Usage
1. Click "Choose Folder" and grant access.
2. Hover segments to inspect size and contents in the side panel.
3. Click a segment to zoom; use breadcrumbs or "Zoom Out" to go back.
4. Use the Layout selector to switch between Flame and Radial views.

## Notes and Limitations
- Browsers cannot access protected system folders due to sandboxing.
- All scanning happens locally in your browser; no data is uploaded.
- Folder upload mode reports file sizes but may omit some metadata.

## Project Structure
- `index.html` - UI, scanner, and visualization logic

## License
MIT. See `LINCENSE.md`.
