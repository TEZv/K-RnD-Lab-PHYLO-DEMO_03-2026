# C1 Master Prep Analytics

A CSV-first prep case for magistracy admission workflows. This section is intentionally lightweight: learn from existing sources, practice on existing platforms, log what you did, and open one clean dashboard for summaries.

## Folder map

- `data/resource_catalog.csv`
  A categorized map of sources for TZNK, English, and IT.
- `data/study_log_template.csv`
  A template for theory / review / concept-study blocks.
- `data/session_log_template.csv`
  A template for practice, simulation, and review sessions.
- `dashboard/`
  A static browser dashboard that reads those CSV files and visualizes the current prep picture.

## Suggested workflow

1. Pick one resource from `resource_catalog.csv`.
2. Study for 15-45 minutes.
3. Add one row to `study_log_template.csv`.
4. Run a test batch on an external platform or in your own trainer.
5. Add one row to `session_log_template.csv`.
6. Open `dashboard/index.html` to see metrics, recent entries, and the resource map.

## CSV columns

### Study log

- `entry_id`: unique row id like `study-014`
- `date`: `YYYY-MM-DD`
- `subject`: `tznk`, `english`, or `it`
- `resource_title`: what you used
- `resource_type`: `official_program`, `concept_explainer`, `course`, `video`, `practice_pool`
- `stage`: `orientation`, `foundations`, `review`, `weak_spot`, `revision`
- `minutes`: duration of the study block
- `notes`: what exactly you covered or noticed

### Session log

- `session_id`: unique row id like `session-021`
- `date`: `YYYY-MM-DD`
- `subject`: `tznk`, `english`, or `it`
- `platform`: where you practiced, for example `Osvita.ua`, `Testportal`, `Connected`, `MathCorporation`
- `mode`: `practice`, `simulation`, or `review`
- `questions_total`: how many questions you touched in that run
- `correct`: how many were correct
- `accuracy_pct`: percentage score
- `minutes`: duration of the run
- `session_label`: your internal tag such as `s001`, `wk2-tznk`, `eng-demo-1`
- `notes`: timing, weak spots, topic pattern, or errors

## Resource logic by subject

### TZNK

- Learn first: official block overview, concept explainers, demo PDF
- Practice next: Osvita.ua pools, Connected logic drills
- Use notes to tag weak spots: sets, order, verbal logic, argument tasks

### English

- Learn first: official language program, archive of past master tests, grammar / reading focus
- Practice next: Testportal demo, Osvita.ua pool, MathCorporation as extra drill
- Use notes to tag weak spots: reading, use of English, conditionals, word formation, vocabulary in context

### IT

- Learn first: official IT program, archive of past IT tests, topic-by-topic revision
- Practice next: Osvita.ua IT pools and full tests
- Use notes to tag weak spots: algorithms, SQL, systems, networks, security, software engineering

## Why this section exists in K-R&D Lab

This is not an LMS and not a replacement for official platforms. It is an operating layer for:

- prep evidence
- repeatable logging
- quick visuals
- a future case study about how the prep process actually evolved over time

## Expansion path

Later, the same CSV schema can feed:

- Google Sheets charts
- a richer static dashboard
- Notion tables
- a public case-study page inside K-R&D Lab
