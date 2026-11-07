# deepaksingh98.github.io

Personal site. Plain HTML and CSS, no build step.

## Adding a project

1. Add an icon to `assets/icons.svg` as a new `<symbol id="name">` (6×6 cell grid, see the existing symbols).
2. Copy `projects/latch/` to `projects/name/` and edit the title, text, icon id and links.
3. Add a list item to the Projects section of `index.html`.

Project pages live under `projects/` because a top-level `/name/` path is taken by that repo's own GitHub Pages site.

## Style

Colours, type and figure rules are in [style/STYLE.md](style/STYLE.md). Build figures with [style/plate.py](style/plate.py).

## Preview

```sh
python3 -m http.server 4173
```
