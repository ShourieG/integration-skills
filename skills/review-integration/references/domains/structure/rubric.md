# Severity rubric -- structure domain

> **Not for single-pass reviews.** This file is one domain's slice of
> `../../severity-rubric.md`, written for a reviewer that owns only this
> domain within a larger, domain-split review. If you are running the
> `review-integration` skill end to end, read the monolith instead -- it
> carries every domain's rows and is the authoritative copy.

Severity definitions and the new-vs-existing calibration note live in
`../severity-core.md`. Read that file first, then the rows below.
Conflicts for this domain: core only (`../conflicts-core.md`); there is no
structure-specific conflict file. The first-version-leniency entry in the
core file matters most to this domain.

> **Maintenance:** these rows mirror the manifest and changelog rows in
> `../../severity-rubric.md`. A PR that changes a row must change both
> files in the same PR.

## Universal rules (same severity regardless of package age)

| Domain | Finding | Severity |
|--------|---------|----------|
| Manifest | format_version too low for features used | HIGH |
| Manifest | conditions.kibana.version too low for agent features used | HIGH |
| Manifest | Data stream duplicates root manifest fields | MEDIUM |
| Changelog | `pull/99999` development placeholder link not replaced with the real PR number | MEDIUM |

## Rules with new-vs-existing severity adjustment

No structure-domain rows carry a new-vs-existing adjustment today. Rows
land here when they exist in `../../severity-rubric.md`.
