# Weekly Data Series

A recurring weekly project: pick a new public dataset, run it through a full ETL and analysis pipeline, and publish the findings. Each week lives in its own folder with the raw data, cleaning script, analysis, and final charts.

Posted weekly on LinkedIn under `#WeeklyDataBreakdown`.

## Why this exists

Practicing end-to-end data work, extraction, cleaning, analysis, and communicating findings to a non-technical audience, on a real cadence instead of one-off tutorials.

## Repo Structure

```
weekly-data-series/
  README.md
  tracker.csv                     <- log of every week: dataset, post link, engagement
  2026-07-21_nyc-hpd-complaints/
    content.md                    <- that week's questions and findings
    hpd_complaints_analysis.ipynb <- full pipeline: pull, clean, analyze, chart
  2026-07-28_next-dataset/
    ...
```

Each week's folder is self-contained: `content.md` has the questions/writeup, the notebook has the full pull-clean-analyze-visualize pipeline.

## Weeks

| Week | Dataset | Domain | Post |
|---|---|---|---|
| 2026-07-21 | NYC HPD 311 Housing Complaints | Government / Housing | [link] |

---

## Week 1: NYC HPD Housing Complaints (July 2026)

**Source:** [NYC Open Data — 311 Service Requests](https://data.cityofnewyork.us/resource/erm2-nwe9.json), filtered to HPD (Department of Housing Preservation and Development) complaints, pulled via the Socrata API.

**Stack:** Python, pandas, matplotlib

Full questions, findings, and write-up: [`content.md`](./2026-07-21_nyc-hpd-complaints/content.md)
Full pipeline (pull, clean, analyze, chart): [`hpd_complaints_analysis.ipynb`](./2026-07-21_nyc-hpd-complaints/hpd_complaints_analysis.ipynb)

---

## Setup

```bash
git clone <repo-url>
cd weekly-data-series/<week-folder>
pip install pandas matplotlib requests
jupyter notebook hpd_complaints_analysis.ipynb
```

## Log

Full history of datasets, post links, and engagement is tracked in [`tracker.csv`](./tracker.csv).
