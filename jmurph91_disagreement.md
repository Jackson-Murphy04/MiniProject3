# MiniProject 3 — Part 2 Disagreement Report

## Scope and method

This report compares the two Part 1 validation logs: Jackson Murphy’s latest generated `jmurph91_validation_log.csv` (Jackson validating Tristan’s projects) and Tristan Lopez’s `tlopez7_validation_log.csv` (Tristan validating Jackson’s projects). The resolution CSV includes every row marked `No` in the pre-discussion agreement column. Proposed values are evidence-based working recommendations, **not claims that Jackson and Tristan have discussed or mutually accepted them**. The partner discussion step remains to be completed.

## Disagreement totals

- Jackson’s log: 7 recorded disagreements.
- Tristan’s log: 15 recorded disagreements.
- Total listed in `disagreement_resolution.csv`: 22.

The CSV is the complete row-level list; the examples below explain representative cases and why the proposed value follows the guide/evidence.

## Example 1 — `gavinsimpson_permute`, `HasRecovered`

- **Author value:** `Partially`; **validator value:** `Yes`; **proposed value:** `Yes`.
- **Evidence:** the recorded longest gap is 31 months (April 2019–October 2021), followed by bug #28 work and CRAN/CI/documentation maintenance.
- **Rationale:** the Coding Guide asks for a binary Yes/No classification. “Partially” is not a valid final category, and the evidence indicates activity resumed after the long gap, so `Yes` is the most defensible normalized value.

## Example 2 — `jasp-stats_jasp-desktop`, `HasRecovered` and `WhyRecovered`

- **Author value for HasRecovered:** `Yes`; **validator value:** blank; **proposed value:** `No`.
- **Evidence:** the recorded longest gap is only one month and does not meet the three-month inactivity threshold; the timeline reports no qualifying gap.
- **Rationale:** recovery requires a qualifying inactivity period followed by renewed activity. Without a qualifying gap, a recovery cannot be established; the associated `WhyRecovered` value should therefore be `N/A`, not a cause inferred from ordinary ongoing activity.

## Example 3 — `bmclab_bmc`, `ActivityPattern`

- **Author value:** `irregular`; **validator value:** `declining`; **proposed value:** `declining`.
- **Evidence:** yearly commit counts peak at 620 in 2018 and then fall substantially across later years (201, 223, 90, 62, 58, 17, 8 through 2025).
- **Rationale:** although annual counts fluctuate, the overall long-term trajectory is downward. `Declining` captures the dominant pattern more directly than `irregular`; this should be confirmed with the project owner during discussion.

## Example 4 — `angel-ml_angel`, `RecentThemes`

- **Author value:** `Other:Feature development`; **validator value:** `Feature development:Documentation updates`; **proposed value:** `Feature development:Documentation updates`.
- **Evidence:** the recorded last-10-commit summary includes a feature implementation, a documentation update, and a license fix; the evidence summary says five of the ten commits are feature development.
- **Rationale:** map themes to the Coding Guide’s defined categories and select the two best-supported themes. Before final submission, verify the actual ten most recent commits and ensure the output format is consistent (the current logs use colon separators in some rows and semicolon separators in others).

## Important data-quality checks before submission

1. Several rows in Jackson’s latest log use `Not reported in source project statistics` in `AuthorValue` rather than leaving the author value blank. Treat that as a missing-data note, not as a literal author-coded category.
2. Tristan’s log has some agreement-status values that should be checked against the actual values. For example, a blank author/validator value may be marked `Yes`, while the JASP `HasRecovered` row has author `Yes`, blank validator value, and status `No`.
3. `RecentThemes` must be grounded in the most recent ten commits. The supplied gap-commit summaries are useful for recovery rationale but do not, by themselves, validate recent themes.
4. Keep `PreDiscussAgreementstatus` as the pre-discussion record. Do not change it to `Yes` merely because a proposed adjudicated value has been chosen. Fill final adjudication/comments only after the partner discussion, if the assignment requires mutually agreed resolutions.

## Files produced

- `combined_adjudicated_validation_log.csv` — both logs combined with proposed adjudicated values and comments.
- `disagreement_resolution.csv` — every recorded disagreement and a proposed resolution rationale.
- `agreement_statistics.csv` — agreement/disagreement counts and rates by field and source log.
