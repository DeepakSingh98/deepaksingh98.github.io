# Site style

The house style for this site, the Latch site and every future article. The reference is the figure set in
[projects/mult-min-net/](../projects/mult-min-net/). When a rule here and those figures disagree, match the figures
and fix this file.

The idea in one line: **dark paper, one serif headline, flat square marks, one bright colour for the thing the figure
is about, everything else quiet.**

## Colour

| Token | Dark | Light | Job |
|---|---|---|---|
| paper | `#151513` | `#f8f6f0` | Page and plate background |
| ink | `#ecebe5` | `#1a1b1a` | Titles, values, primary text |
| ink-2 | `#c9c7bf` | `#3b3d39` | Body text |
| mute | `#9a988f` | `#6a6c64` | Subtitles, axis labels, captions |
| rule | `#2f2e29` | `#e2ded3` | Page dividers |
| wash | `#21201d` | `#efebe1` | Hover fills, code backgrounds |
| orange | `#ff8a3d` | `#b44f0a` | The subject |
| blue | `#45a8ff` | `#1b6fc4` | Second series, cost, waiting, negative |
| green | `#6fd08c` | `#1f8a52` | Third series only |

Plate-only colours, always the dark values: base `#77766e` (the baseline being compared against), cell `#2b2a26`
(empty cells, memory bars), grid `#2a2925`, axis `#55534c`.

Colour roles:

- **Orange is the subject.** A single-series chart is orange. In a comparison, your thing is orange and the baseline
  is base gray. Latch is orange everywhere, including diagrams.
- **Blue is the counterpart.** Use it for negative weights, a second series, or cost such as barriers and waits.
- **Green appears only when a figure truly has three categories.** Never add a fourth hue. Fold extra categories into
  gray or use small multiples.
- **When all three hues are categories**, mark the subject with an ink outline instead of a colour, as in
  `nestor-structure.svg`.
- **Colour follows the entity across a page.** If "attention" is blue in one figure, it is blue in the next.
- **Text stays in ink or mute,** never a series colour. Put a square swatch next to the label instead.
- If a caption names a colour ("orange bars"), recheck it whenever the palette mapping changes.

## Type

No web fonts, on either site.

| Role | Face | Setting |
|---|---|---|
| Page title | Serif | 400, 2.6 to 3.25rem, tight tracking |
| Section heading (`h2`) | Serif | 400, 1.6rem |
| Lede | Serif | 400, 1.3rem |
| Sub-heading (`h3`) | Sans | 500, about 1.05rem |
| Body | Sans | 16px / 1.65, 40 to 42rem column |
| Caption | Sans | 0.85rem, mute |
| Code, numbers in figures | Mono | |

Serif stack: `"Iowan Old Style", Charter, "Bitstream Charter", "Sitka Text", Cambria, Georgia, serif`.
Sans stack: the system stack. Mono stack: `ui-monospace, SFMono-Regular, Menlo, Consolas, monospace`.

## Figures

Every figure is a **plate**: a 16:9 dark image that stands on its own when screenshotted into a post.

- **Size:** 1200×675 SVG, or 1920×1080 PNG from matplotlib. Export a 2x PNG when it will be used as a link preview.
- **Always dark.** Plates keep the dark palette in the light page theme, so they work as `<img>` and in link previews.
  Do not use `prefers-color-scheme` inside an SVG figure.
- **Header:** serif title at top left, stating the result in a few words ("Stopping when it's done"). One muted sans
  subtitle says what is being shown. No bold titles.
- **Footer:** one muted note at bottom left for conditions, and the legend at bottom right.
- **No panels.** No cards, boxes, drop shadows or gradients. Marks sit straight on the paper.
- **Square marks.** No rounded corners on bars, cells or swatches.
- **Show the real object when you can.** Weight matrices as cells, attention as cells, kernels as blocks. A grid of dim
  `#2b2a26` cells with a few bright ones is the signature look.
- **Label directly.** Put the name and value at the mark ("Latch 8.2 h", "median 15"). Thin lead lines are fine. Values
  use mono. Do not number every point.
- **Gridlines recede:** 1 to 1.5 px in grid colour. Only the baseline gets the axis colour. No top or right spines.
- **Reference lines** are dashed ink ("before the edit: always 42 passes").
- **Arrows** are thin. Ink when they carry the argument, base gray when they are structure.
- **Scales are honest.** Bars start at zero. No dual axes. If panels use separate scales, the note says so.
- **Alt text carries the numbers.** Put them in the SVG `<desc>` and in the `<img alt>`.

## Pages

- Dark by default, with a toggle to light. Both sites share `assets/theme.js` behaviour and the `theme` storage key.
- Links inherit the text colour with a muted underline, which turns orange on hover. Orange is also the focus ring and
  text selection.
- Plates run 56rem wide on desktop and captions stay on the reading column. On phones they fit the column.
- In the light theme plates get a 10px corner radius. In the dark theme they melt into the page.
- Tables are rules only: no fills, no vertical lines, right-aligned tabular numbers.
- Project icons are 6×6 cell grids in `assets/icons.svg`.

## Making a figure

SVG, for bars, diagrams and anything built from cells:

```python
import sys; sys.path.insert(0, "style")   # or copy plate.py next to the script, as Latch does
from plate import Plate

p = Plate("Where the time went", "One-line subtitle.", desc="Alt text with the numbers.")
p.rect(396, 186, 640, 44, "orange")
p.note("Conditions go here.")
p.legend([("Latch", "orange"), ("PyTorch", "base")])
p.save("figures/name.svg", png="figures/name.png")
```

matplotlib, for dense scientific plots: call `plate.use_matplotlib()` first, then pass `plate.COLORS` values to your
marks. Title with a serif `fig.text`, subtitle in mute.

`site/figures/make_figures.py` in the Latch repo has worked examples of grouped bars, small multiples, a line chart with
end labels, and a structure diagram.

## Before publishing

1. Open the figure at article width and read the smallest text. It should still be legible at 680px wide.
2. Check for label collisions and clipped text.
3. Check the page in both themes and at phone width.
4. In Latch, recompute `SOURCE_SHA256SUMS` and `RELEASE_MANIFEST.json` for every changed site file.

The palette passes the dataviz validator's colourblind separation, normal-vision and contrast checks on `#151513`.
It sits above the validator's dark-mode lightness band on purpose, because the brightness is the look.
