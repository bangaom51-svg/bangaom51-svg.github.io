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

## Editing a handout

1. Edit `lab-N/index.md`.
2. Add a row to the revision history at the bottom of that file. Students are told
   to check it, so a change without a row is a change nobody knows about.
3. Commit and push. The site rebuilds in roughly a minute.

If a correction affects grading — a deliverable filename, a due date — announce it
on Canvas and Discord as well. Do not rely on students re-reading a page they have
already read.

## Figures

Screenshots go in `assets/lab-N/` and are referenced as
`![caption](../assets/lab-N/name.png)`.

## Local preview (optional)

    bundle exec jekyll serve

Not required. Pushing and looking at the live site is usually faster.
