# CSCE 616 / 700 — lab handouts

Source for the course handout site published with GitHub Pages at
<https://csce-616-fa26.github.io/>.

This repository is **public** — GitHub Pages on a free organization only serves
from public repositories. Handouts are not secret; solutions live in the private
`lab-N-solution` repositories and must never be added here.

## Why handouts live here rather than in the starter repos

Classroom 50 copies the starter repository at the moment a student accepts the
assignment. Anything committed to a starter repo is therefore a snapshot: editing
it later changes what future accepters receive and nothing else. A student who
accepted on Monday keeps reading Monday's text all week.

A handout served from this site has one stable URL. Pushing a correction updates
what every student reads, including those who accepted days earlier — the same
property the Google Docs handouts had, with version history and diffs added.

The starter repositories carry only a short README pointing here.

## Adding a lab

1. Copy `LAB-TEMPLATE.md` to `lab-N/index.md`.
2. Fill in the front matter — `lab_number`, `lab_title`, `released`, `due`.
3. Write the body. Sections 1–7 are fixed and always appear in the same order,
   so students learn the shape once and it holds for every lab.
4. Add a row to the table in `index.md`.
5. Run the audit, then push.

```bash
python3 tools/audit.py
```

## Design system

There is no remote theme. `_layouts/` and `assets/css/main.css` are the whole
design, kept local so a GitHub Pages change cannot silently restyle a handout.

`main.css` is token driven and the tokens are the contract:

- **Colour** — every value is a custom property on `:root`, with a full dark
  counterpart under `prefers-color-scheme: dark`. No literal hex outside those
  blocks except in `@media print`, which deliberately forces black on white.
- **Contrast** — 4.5:1 for all text in both themes, 3:1 for the focus ring and
  for `--border-strong`. Verified, not assumed. `--border` is deliberately below
  3:1: it draws decorative rules, and WCAG 1.4.11 governs interactive
  boundaries, of which this design has none defined by a border alone.
- **Type** — a 1.200 scale, fluid via `clamp()` at the larger sizes. Body text is
  capped at a 68-character measure; tables, figures and code break out of it.
- **Space** — a single 4px-based scale, `--sp-1` through `--sp-9`. No ad hoc
  margins.

## Accessibility

The site is built to WCAG 2.1 AA. What that means concretely here:

- A skip link, one `<h1>` per page, and heading levels that never skip.
- Every figure is a `<figure>` with alt text describing the image and a
  `<figcaption>` explaining it — never the same sentence twice.
- Focus is never removed, only restyled, at 3:1 against its background.
- Nothing is carried by colour alone; links are underlined.
- `prefers-reduced-motion` is honoured.
- Wide tables become keyboard-reachable scroll regions with an accessible name
  (`assets/js/enhance.js`). That script is progressive enhancement only — the
  page is complete and navigable with JavaScript disabled.

`tools/audit.py` enforces the structural half of this on every run.

## Editing a handout

1. Edit `lab-N/index.md`.
2. Add a row to the revision history at the bottom of that file. Students are told
   to check it, so a change without a row is a change nobody knows about.
3. Run `python3 tools/audit.py`.
4. Commit and push. The site rebuilds in roughly a minute.

If a correction affects grading — a deliverable filename, a due date — announce it
on Canvas and Discord as well. Do not rely on students re-reading a page they have
already read.

## Figures

Screenshots go in `assets/lab-N/` and are referenced from `lab-N/index.md` as
`../assets/lab-N/name.png`.

## Local preview

The ECE cluster has no Ruby, so there is no local Jekyll build. `tools/audit.py`
covers what a build would have caught; beyond that, push and look at the live
site.
