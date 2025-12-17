# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repo is

This is the **GitHub profile repository** (`su6i/su6i`). The `README.md` at the root is what GitHub renders on [github.com/su6i](https://github.com/su6i). There is no build system, no package manager, and no test suite.

## Key files

- `README.md` — the public-facing profile page; edits here are immediately visible on GitHub
- `assets/linkedin_su6i.svg` — LinkedIn badge SVG used inline in the README
- `.github/workflows/update-readme.yml` — scheduled GitHub Action (daily at midnight UTC) that auto-updates the `<!--START_SECTION:activity-->` / `<!--END_SECTION:activity-->` block via `jamesgeorge007/github-activity-readme`

## Editing the profile

The README uses raw HTML mixed with Markdown. The `<div align="center">` wrappers are intentional — GitHub renders them for centering. GitHub stats cards are pulled from external services (github-readme-stats, streak-stats.demolab.com) at render time; no local build step is needed.

The activity section between the `<!--START_SECTION:activity-->` and `<!--END_SECTION:activity-->` comments is **overwritten automatically by the workflow** — do not manually edit content between those markers.

To trigger the activity update manually without waiting for the cron, run the workflow from the GitHub Actions tab using `workflow_dispatch`.
