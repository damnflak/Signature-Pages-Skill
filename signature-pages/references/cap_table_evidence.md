# Cap Table Evidence

Use this reference only for cap-table reading support needed by signature-page work.

## Boundary

Cap-table evidence helps identify shareholders, shareholder-like rights, series participation, party groups, and checklist gaps. It is auxiliary cross-check evidence only. It does not replace legal-document review, does not decide final signing requirements by itself, and cannot create a signing obligation for a specific file.

Do not import Financials Normalizer as a dependency, nested skill, script package, banker workflow, valuation process, financial-statement normalizer, EBITDA/net debt routine, public-market workflow, or model deliverable.

## Read-Only Workbook Handling

- Preserve the original workbook and source package.
- Ignore temporary lock files and obvious non-source artifacts.
- Do not overwrite, rename, hide, delete, or destructively transform raw workbook tabs.
- Write extracted shareholder/right tables and QA notes into the signature-page work/output area.

## Source Locators

For every extracted cap-table fact, record:

- `source_id`
- Workbook/file name
- Sheet name
- Row number
- Column name or column letter
- Cell or range
- Source value exactly as shown
- Displayed/calculated value if different
- Formula text where applicable
- Extraction note and confidence

Use locators for shareholder names, share counts, security/right classes, percentages, SAFE conversion outputs, warrant information, ESOP/reserve rows, series/entry round, and totals/tie-outs.

## Structured Shareholder/Right Table

Build a cap-table-derived table with these fields when available:

| Field | Purpose |
| --- | --- |
| `raw_shareholder_name` | Name as shown in the workbook. |
| `short_name` | Working short form for guidance and filenames. |
| `full_name_candidate` | Candidate legal name, later checked against SHA schedules. |
| `english_name` / `chinese_name` | Supports required name matrix. |
| `security_or_right_class` | Ordinary shares, preferred shares, SAFE, warrant, ESOP/reserve, or similar right. |
| `share_count_or_equivalent` | Shares or equivalent rights. |
| `percentage` | Ownership or conversion percentage when available. |
| `series_or_entry_round` | Supports old/new/both investor grouping. |
| `reported_or_calculated` | Distinguish source-reported value from formula-derived calculation. |
| `formula` | Formula text if relevant. |
| `displayed_value` | Workbook-calculated/displayed value. |
| `party_group_candidate` | Old investor, new investor, company side, shareholder-like right, ESOP/reserve, or open. |
| `source_id` / `source_location` | Review traceability. |
| `qa_flag` / `open_question` / `confidence` | Missing, conflicting, or uncertain item handling. |

## Shareholder-Like Rights

For private-equity transaction-document purposes, count SAFE, warrants, and similar shareholder-like rights together with shares when they carry rights similar to shareholders.

Practical rules:

- Include SAFE and warrant holders in party discovery and checklist review.
- Preserve whether the right is an actual share, convertible instrument, warrant, ESOP/reserve, or other right.
- Do not convert a shareholder-like right into a signing party unless transaction documents, schedules, or user instructions support that party signing a document.

## Reported, Calculated, Missing, And Conflicting Values

- Label values directly visible in the cap table as reported/source values.
- Label formula-derived values, SAFE conversions, percentages, totals, and tie-outs as calculated or derived.
- Preserve both formula and displayed value when formulas affect shares, percentages, SAFE conversion, warrants, ESOP/reserve, or ownership changes.
- Leave unsupported values blank or mark them as missing/open.
- Preserve conflicting values across sheets, versions, or schedules; do not silently choose one unless the source hierarchy and explanation rules justify a working value.

Useful evidence labels:

- `source_reported`
- `derived_calculation`
- `user_provided_assumption`
- `inferred_low_confidence`
- `missing_required_source`

## QA Flags

Flag these issues before using cap-table evidence downstream:

- Missing full legal name.
- Unclear short name or duplicated short name.
- Inconsistent shareholder name across cap table and SHA schedules.
- Inconsistent percentages, non-tying totals, or formula errors.
- Unclear series or entry round.
- Hidden rows, merged cells, blank headers, subtotals, or rows that are not real parties.
- SAFE/warrant/ESOP rows whose legal signing relevance is unclear.
- Stale workbook version or conflicting sheets.
- Missing sheet/cell source locator.

## Handoff To Signature-Page Decisions

Use cap-table extraction to:

- Populate the name matrix and investor grouping candidates.
- Check old/new/both investor classification.
- Cross-check SHA investor series labels, including multiple applicable series, only after those labels are tied back to SHA schedules or other current-file source-supported evidence.
- Cross-check SPA current-round investor grouping and ODI/Non-ODI review only after those labels are tied back to the SPA schedule or other current-file source-supported evidence.
- Identify shareholder-like rights that may need legal-document cross-check.
- Support copy/signature count override review when the cap table or source instruction supports it.
- Create open questions for missing or inconsistent shareholder/source facts.

Do not use cap-table math or cap-table party lists to decide signer title, seal requirement, hand-sign requirement, document-specific role, final party obligation, or final signature-page capacity label without current-file support. For SHA/SPA, schedules are the direct drafting source for identity groups; the cap table can only confirm, conflict-check, or raise open questions.
