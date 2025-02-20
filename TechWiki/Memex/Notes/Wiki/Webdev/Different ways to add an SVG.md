---
tags: webdev, svg
category: wiki
---

## Set as source on an image element
Pro:
- can be buffered by browser

## Add as background image with CSS

## Inline SVG into HTML
Pro:
- you don't need an extra request, SVG is right there
Con:
- can't be buffered/reused

-> Good for SVG that are part of the first render.
Not good for larger SVGs or images that are repeatedly used.