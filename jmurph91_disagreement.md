# MiniProject 3 — Part 2 Disagreement Report

## Scope and method

This report summarizes the comparison of Jackson Murphy’s and Tristan Lopez’s Part 1 validation logs. The original `PreDiscussAgreementstatus(Yes/No)` values are retained as a record of independent coding before discussion. All recorded disagreements were discussed and resolved by agreement; the final decisions are recorded in `combined_adjudicated_validation_log.csv` and listed individually in `disagreement_resolution.csv`.

## Disagreement totals

- Jackson’s validation log: 7 pre-discussion disagreements.
- Tristan’s validation log: 15 pre-discussion disagreements.
- Total: 22 disagreement rows, all with a final adjudicated value.

The agreement statistics file reports the original pre-discussion agreement rates by field. These rates are not changed by the later adjudication process.

## Example 1 — `gavinsimpson_permute`, `HasRecovered`

- **Author value:** `Partially`; **validator value:** `Yes`; **final adjudicated value:** `Yes`.
- **Evidence:** the project had a recorded 31-month gap from April 2019 to October 2021, followed by work on bug #28 and CRAN, CI, and documentation maintenance.
- **Resolution:** the Coding Guide requires a binary Yes/No value. “Partially” is not a valid final category, and the post-gap evidence shows activity resumed, so both partners selected `Yes`.

## Example 2 — `bmclab_bmc`, `ActivityPattern`

- **Author value:** `irregular`; **validator value:** `declining`; **final adjudicated value:** `declining`.
- **Evidence:** yearly commit counts peak at 620 in 2018 and then fall substantially across later years (201, 223, 90, 62, 58, 17, and 8 through 2025).
- **Resolution:** although annual counts fluctuate, the overall long-term trajectory is downward. The partners selected `declining` as the category that best captures the dominant pattern.

## Example 3 — `angel-ml_angel`, `RecentThemes`

- **Author value:** `Other; Feature development`; **validator value:** `Feature development; Documentation updates`; **final adjudicated value:** `Feature development; Documentation updates`.
- **Evidence:** the recorded recent-commit summary identifies feature implementation and documentation work among the latest ten commits, alongside a license fix.
- **Resolution:** the partners selected the two most representative Coding Guide categories and standardized the separator as a semicolon.

## Overall findings

The most common disagreements involved interpreting recovery after a long inactivity gap, choosing one overall activity-pattern label, and selecting the two most representative recent-commit themes. Applying the Coding Guide consistently helped turn descriptive or nonstandard values into comparable categories while retaining the original independent-coding record. The final adjudications and rationale are documented row by row in the CSV deliverables.

## Deliverables

- `combined_adjudicated_validation_log.csv` — both validation logs with final adjudicated values and comments.
- `disagreement_resolution.csv` — all 22 pre-discussion disagreement rows and their final resolutions.
- `agreement_statistics.csv` — agreement and disagreement counts by field and source log, based on the original pre-discussion statuses.
- `validation_reflection.md` — reflection on the validation and resolution process.
