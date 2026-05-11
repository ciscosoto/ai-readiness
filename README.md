# SPRO AI Readiness

An editorial dashboard for the AI readiness of Cisco's Strategy, Planning & Revenue Operations org. Quadrant chart, four markers of movement, a twelve-badge progression system, and development plans by quadrant.

## Stack

A single self-contained HTML file — markup, CSS, and JS all inline. No build step, no dependencies. Open `index.html` directly in a browser, or attach/AirDrop the file to share.

The only external request is to Google Fonts (Source Serif 4 + Inter). Offline use degrades gracefully to system fonts.

## Editing

Everything lives in `index.html`:

- **Distribution clusters** → `CLUSTERS` array in the `<script>` block (counts, centers, spreads)
- **Quadrant copy and development plans** → `QUADRANTS` object
- **Badges** → `BADGES` array
- **Section prose** → the markup inside `<div class="wrap">`
- **Visual design** → the `<style>` block in `<head>`

## Notes

The current dataset (200 positions matching SPRO headcount) is synthetic, generated deterministically from cluster definitions. Replace `generatePositions()` when integrating with the live pulse + telemetry feed.
