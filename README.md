# modern-sas

Public-facing Quarto **course-materials site** for **Modern SAS for
Statistical Analytics**, assembled by Matt Hester. Sibling to the main
site [matthewhester.com](https://matthewhester.com); intended to live at
`/modern-sas/` under that domain.

This is **assembled course material** — synthesized lesson notes,
hands-on SAS labs, and curated references. It is a durable public
resource site, **not** a record of a currently scheduled section, and
**not** an LMS.

## Status

Assembled from a course-material build (2026-06). Topic flow, notes,
labs, and resources are in place. Dates, weights, and final policies are
not sealed and are authoritative in the LMS whenever the course runs.
Treat the site as a coherent draft, not a final release.

## What this site holds

- **Notes** — the weekly instructional spine (15 weeks, four parts): the
  SAS analytics environment, libraries/datasets/formats, DATA step
  logic, importing/cleaning/validating, PROC SQL and joins, summaries
  and tables, ODS output and visualization, the core statistical
  procedures (TTEST, GLM/ANOVA, REG, LOGISTIC), reshaping/merging,
  simulation, and a reproducible analysis report.
- **Labs** — four hands-on SAS labs (build & validate a DATA step, PROC
  SQL joins, linear regression & diagnostics, simulation).
- **Resources** — a SAS workflow glossary, a PROC reference, a log-and-
  verification guide, and a SAS academic-access & project-setup page.

The notes are the course's **own synthesis**. The recurring study, SAS
code, logs, and PROC output are **hand-authored synthetic listings**
(no SAS engine was run). Statistical-background pointers cite
*Introduction to Modern Statistics* (CC BY-SA 3.0); official SAS
documentation is **proprietary (© SAS Institute Inc.)** and is linked
and cited only — never reproduced. **SAS® and all SAS Institute product
names are the property of SAS Institute Inc.**

## What does not go in this repo

Anything private to a graded offering: answer keys, assessment items,
rubrics, point values, due dates, student data, or any directory from
the private course build (`_state/`, `assessment_shadow/`,
`source_text/`, `run_reports/`, `accessibility/`). See
[`CLAUDE.md`](CLAUDE.md) for the full list. The operational, graded side
of any live offering lives in **Blackboard (the LMS)**, which is
authoritative.

## Local development

```bash
quarto render     # build to _site/
quarto preview    # live preview
```

SAS code is shown as **static, non-executed** ` ```sas ` fences (logs
and PROC output are hand-authored synthetic listings), so the site
renders **fully with plain `quarto render` — no SAS engine and no R
required**.

## Layout

```
modern-sas/
├── _quarto.yml              # site config, navbar, sidebar, render allow-list
├── index.qmd                # landing page (hero + overview)
├── syllabus.qmd             # public course overview
├── schedule.qmd             # week-by-week topic map
├── notes/                   # weekly instructional notes + index
├── labs/                    # hands-on SAS labs + index
├── resources/               # glossary, PROC reference, log/verification, access + index
├── assets/                  # hero.png + icon.png (course identity art)
├── styles.css               # course-family palette
├── CLAUDE.md                # privacy + editing rules
└── README.md                # this file
```

No CI and no deploy pipeline in this repo. The combined site is
assembled and deployed by the hub repo (`matthewhester-site`). Local
builds only here; commits are deliberate and user-driven.
