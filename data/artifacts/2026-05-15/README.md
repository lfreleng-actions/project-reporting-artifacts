# Gerrit Reports - 2026-05-15

Generated on: 2026-05-15 08:00 UTC (recovered 2026-05-19)

## Summary

- **Date**: 2026-05-15
- **Total Artifacts**: 15
- **Total Files**: 55
- **Workflow Run**: [25907123397](https://github.com/lfreleng-actions/project-reporting-tool/actions/runs/25907123397)

## Recovery Note

This folder is a **partial recovery** of artifacts that were never
transferred to this repository on 2026-05-15. The original Production
Reports workflow run (25907123397) failed because:

- The `fdio` matrix entry failed at `actions/upload-artifact` (the
  GitHub Actions artifact service returned an HTML error page instead
  of JSON — a transient upstream service condition).
- The `lfit` matrix entry never started (no runner ever picked it up;
  conclusion remained `null`).

The combined effect caused `needs.analyze.result` to be neither
`success` nor `failure`, so the existing `if:` guards on the
`Publish GitHub Pages` and `Transfer/Copy Artifacts` jobs evaluated
to false and both were skipped. As a result, no artifacts for
2026-05-15 were transferred at the time.

The artifacts present here are the five projects that did succeed
on 2026-05-15 (agl, lfbroadband, odl, onap, oran), recovered from
the re-run on 2026-05-19. The `fdio` and `lfit` artifacts are
**not present** for this date because their underlying data only
ever existed from the 2026-05-19 re-run, not from the original
2026-05-15 trigger.

The workflow itself has been hardened in
lfreleng-actions/project-reporting-tool#185 so this failure mode
cannot silently drop data again.

## Contents

This directory contains all artifacts from the production reports
workflow run.

Each subdirectory corresponds to a workflow artifact:
- `reports-<slug>`: Generated report files (HTML, Markdown, JSON)
- `raw-data-<slug>`: Raw data JSON files
- `clone-manifest-<slug>`: Repository clone manifests

## Artifacts

- **clone-manifest-agl**: 1 files
- **clone-manifest-lfbroadband**: 1 files
- **clone-manifest-odl**: 1 files
- **clone-manifest-onap**: 1 files
- **clone-manifest-oran**: 1 files
- **raw-data-agl**: 3 files
- **raw-data-lfbroadband**: 3 files
- **raw-data-odl**: 3 files
- **raw-data-onap**: 3 files
- **raw-data-oran**: 3 files
- **reports-agl**: 7 files
- **reports-lfbroadband**: 7 files
- **reports-odl**: 7 files
- **reports-onap**: 7 files
- **reports-oran**: 7 files
