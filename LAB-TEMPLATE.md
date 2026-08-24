---
layout: lab
title: "Lab N — Short Title"          # browser tab and search results
lab_number: N
lab_title: "Short Title"              # rendered as the page H1
course: "CSCE 616 / 700 · Introduction to Hardware Design Verification"
term: "Fall 2026"
instructor: "David Kebo Houngninou"
released: "Monday, Month D, YYYY, 9:00 AM CT"
due: "Monday, Month D, YYYY, 11:59 PM CT"
notice: >
  This page is the authoritative version of the handout and may be corrected
  after release. The copy in your assignment repository does not update. Check
  the revision history at the bottom before you submit.
description: "One sentence describing the lab, used for search results and link previews."
---

<!-- =====================================================================
     LAB HANDOUT TEMPLATE
     Copy this file to lab-N/index.md and fill it in.

     Structure is fixed on purpose: students learn where to look once and
     that knowledge carries to every later lab. Sections 1-7 always appear,
     in this order, even when a section is short.

     House rules
       - One H1 only; it comes from the front matter, not the body.
       - Sections are H2 and numbered. Subsections are H3 and numbered x.y.
       - Every figure is a <figure> with real alt text AND a <figcaption>.
         Alt describes what is in the image; the caption says what it means.
         They must not be the same sentence.
       - Tables are written as markdown. The build adds column scopes and,
         when a table is too wide for the screen, makes it a keyboard
         reachable scroll region named after the heading above it. So put
         every table under a heading that describes it.
       - Never write "see the image below" or "click the green button":
         position and colour are not available to every reader.
       - Code blocks are fenced and language tagged.
       - Any change after release adds a row to the revision history.
     ===================================================================== -->

<nav class="toc" aria-labelledby="toc-heading" markdown="1">
## On this page
{: #toc-heading .toc__heading .no_toc}

1. TOC
{:toc}
</nav>

## 1. Objectives

By the end of this lab you will be able to:

1. First capability, phrased as something the student can do.
2. Second capability.

## 2. Background

### 2.1 Design under test

What the DUT is and what it does.

### 2.2 Parameters

| Parameter | Value | Meaning |
| --- | --- | --- |
| `NAME` | 0 | What it controls |

### 2.3 Interface

| Signal | Direction | Width | Description |
| --- | --- | --- | --- |
| `sig` | input | 1 | What it does |

## 3. Environment setup

### 3.1 Prerequisites

### 3.2 Log in to the Linux server

### 3.3 Get your repository

### 3.4 Set up the Cadence environment

### 3.5 Repository layout

## 4. Walkthrough

### Part 1 — Guided steps

**Step 1.** Do the thing.

```bash
command here
```

<figure>
  <img src="../assets/lab-N/figN-name.png"
       alt="Describe what is visibly in the screenshot, for a reader who cannot see it.">
  <figcaption>Figure 1 — what this figure is showing and why it matters.</figcaption>
</figure>

### Part 2 — Read the code

## 5. To-do

### Task 1 — Imperative title

What to do, and the reasoning behind it.

## 6. Deliverables

Commit and push all of your changes to your assignment repository. Your
repository must contain:

| # | Path | Description |
| --- | --- | --- |
| 1 | `path/to/file` | What it is |

## 7. Getting help

- **Public questions** — post on the course Discord server. Most setup problems
  have already been answered there.
- **Private questions** — email the TA or the instructor.
- **Office hours and help sessions** — see the syllabus for times.

You may discuss this lab conceptually with classmates. The implementation you
submit must be your own work. See the syllabus for the full collaboration and
academic integrity policy.

## Revision history

Changes made to this handout after release are listed here, newest first.

| Date | Change |
| --- | --- |
| Month D, YYYY | Initial release for Fall 2026. |
