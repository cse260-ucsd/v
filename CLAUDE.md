# Implementation of optimized matrix multiplication

Self-contained interactive HTML pages (no build step) teaching matrix multiply for CPU and GPU.

## GotoBLAS

- `gotoblas.html`

## CUDA

- `cutlass-visualization-v2-naive.html` (Part 1)
- `cutlass-visualization-v2-shared-memory-tiling.html` (Part 2)
- `cutlass-visualization-v2-1d-block-tiling.html` (Part 3)
- `cutlass-visualization-v2-2d-block-tiling.html` (Part 4)

## Decisions

- **No filler text.** Keep only text that carries information: no decorative figure titles, panel labels or "hover for details" hints. Ledes briefly explain the page's one idea.
- **Text mirrors the picture.** When a caption names something the picture marks, mark it the same way in the text.
- **Interactions match the Follow level** (thread / warp / block): hover outlines and highlights cover the followed group's size, and hover must not flicker across gaps between cells.
- **Controls never replay by accident**: stepping past the first or last step does nothing.
- **Small model, real reference.** Pictures use a shrunk GPU (8 × 8 matrices in Part 1, 16 × 16 from Part 2 on; 4-thread warps); each part ends with numbered notes on how a real implementation on a Tesla T4 differs, and the kernel in CUDA C++. Cite and link NVIDIA's official docs (the current CUDA Programming Guide) for facts.
- **One look across pages**: shared CSS tokens, fonts and light/dark themes; C is blue, A orange, B green everywhere (matching `gotoblas.html`).
- **Commit after every change.** Finish each change with a git commit; don't leave edits uncommitted.
