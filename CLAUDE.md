# CUTLASS, step by step

Self-contained interactive HTML pages (no build step) teaching GPU matrix multiply.
Reading order: `cutlass-visualization-v2-intro.html` → Part 1 (`-v2.html`) → Part 2 (`-coalescing`) → Part 3 (`-cache-blocking`), linked by each page's pager.

## Decisions

- **No filler text.** Keep only text that carries information: no decorative figure titles, panel labels or "hover for details" hints. Ledes briefly explain the page's one idea.
- **Text mirrors the picture.** When a caption names something the picture marks, mark it the same way in the text.
- **Interactions match the Follow level** (thread / warp / block): hover outlines and highlights cover the followed group's size, and hover must not flicker across gaps between cells.
- **Controls never replay by accident**: stepping past the first or last step does nothing.
- **Small model, real reference.** Pictures use a shrunk GPU (8 × 8 matrices, 4-thread warps); the intro lists the differences from a Tesla T4. Cite and link NVIDIA's official docs (the current CUDA Programming Guide) for facts.
- **One look across pages**: shared CSS tokens, fonts and light/dark themes; A is blue, B orange, C green everywhere.
