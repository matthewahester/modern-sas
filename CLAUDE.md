# CLAUDE.md — modern-sas (public Quarto site)

_Notes for Claude Code or any AI assistant working in this repo._

## What this repo is

The **public-facing Quarto course-materials site** for **Modern SAS for
Statistical Analytics** assembled by Matt Hester. It is a sibling of the
main site [matthewhester.com](https://matthewhester.com) and is intended
to live at `/modern-sas/` under that domain, alongside the other course
sites.

It holds **assembled course material** — the course's own synthesized
notes, hands-on SAS labs, and curated resources.

## What this repo is not

- It is **not** the private course build. That lives in a separate,
  Drive-synced teaching workspace and is not part of this repository.
- It is **not** a claim that the course is currently being taught. This
  is durable, public course material; honest wording is "assembled
  course materials," not "a course I am teaching now."
- It is **not** the LMS. **Blackboard remains authoritative** for grades,
  due dates, submissions, rosters, and anything operational whenever the
  course runs.
- It is **not** a raw archive, and **not** a mirror of the SAS
  documentation. Lesson pages are the course's own synthesized prose.

## Do not add to this repo

- Answer keys or solutions (any form: PDF, TeX, Markdown, `_key.*`).
- Assessment items, specs, manifests, scenarios, rubrics, point values.
- Anything from the private course build:
  `_state/`, `assessment_shadow/`, `source_text/`, `run_reports/`,
  `accessibility/`, `export/`.
- SAS data sets (`*.sas7bdat`), real or student data, FERPA-adjacent
  material, gradebook exports, rosters.

## SAS attribution (important)

- **SAS documentation is proprietary** (© SAS Institute Inc., all rights
  reserved). Cite and link specific doc pages in the course's own words,
  with at most a short attributed quote — never reproduce or closely
  paraphrase SAS-doc prose, examples, listings, tables, or figures.
- All SAS code, logs, and PROC output on this site are **hand-authored
  synthetic listings** ("as if run"); no SAS engine was invoked. Keep it
  that way — do not paste real run output that could carry copyrighted or
  private content.
- **SAS® and all SAS Institute product names are the property of SAS
  Institute Inc.**

When unsure, default to **don't publish** and ask.

## Provenance

Assembled (2026-06) from a course-material build. Only the public surface
was promoted: `index.qmd`, `syllabus.qmd`, `schedule.qmd`, `notes/`,
`labs/`, `resources/`, `styles.css`, and `_quarto.yml`. Every private
directory listed above was deliberately left behind.

## Rendering

- SAS code is written as **static, non-executed** ` ```sas ` fences, so
  `quarto render` builds the whole site **without SAS and without R**
  (deterministic). Output goes to `_site/` (gitignored).
- The combined public site is assembled and deployed by the hub repo
  (`matthewhester-site`); this repo has no CI of its own.

## Images

- `assets/hero.png` — full course-identity banner (carries the title);
  referenced on `index.qmd` with `.course-hero-img` and alt text.
- `assets/icon.png` — square crystal mark with transparent background;
  wired as the navbar `logo`.
- Every committed image needs alt text.

## Hard rules for Claude in this repo

- **Commit only when explicitly instructed.** Never push without explicit
  instruction.
- **Do not reach back into the private course build** unless explicitly
  instructed.
- **Do not wire up deployment** (CI, remotes, hub workflow edits) without
  an explicit decision.
