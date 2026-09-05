# Signature Page Body Drafting

Use this reference only after the source index, party/file matrices, signing guidance, received trackers, and file-piecing controlling list are complete. Signature-page bodies are the last drafting output.

This file is the entry point for signature-page body drafting. It does not replace the general workflow, source-boundary, output-package, guidance/tracker/piecing, QA, PDF derivative, traceability, sample-leakage, or legal-review rules in the other references.

## Required Body Drafting Order

1. Confirm the file's source decision in the file-party matrix: `existing_real_page`, `generate_from_sources`, `visual_reference_only`, or `open_question`.
2. If the source already contains a real signature page, extract it directly and preserve provenance. Do not generate a substitute unless separately instructed.
3. If a page must be generated, confirm the current file itself supports each signing party. Read the current document's full title, defined term, party definitions, execution clause, signature legends, schedules, signature blocks, and signature roles.
4. Identify the exact document family and execution form, including whether the document is an ordinary agreement, unilateral instrument, written resolutions/written consent, constitutional document, agreement-form side letter, or commitment letter.
5. Identify the execution role on the current page, whether a holder/recipient/accepting party countersigns, the exact special legend if any, and the number of executing legal persons covered by the clause.
6. For SHA/SPA pages, confirm the schedule group trace matrix fields `source_group_label_exact` and `final_capacity_label_for_signature_page` are populated from the SHA/SPA schedules with a source locator. Use those fields for page capacity labels, not party short names or hard-coded investor-name rules.
7. Open [signature_page_body_samples.md](signature_page_body_samples.md) and select the exact document family, document form, execution role, singular/plural variant, and special-legend variant. For SHA/SPA, also read the desensitized-example population notes so exact multi-identity labels are preserved without turning example values into defaults.
8. If a matching variant exists, use that desensitized sample as the direct drafting base. Preserve its complete structure, including in-text header, body sequence, signature block, date/seal treatment, and footer pattern where applicable. Replace only variables supported by the current source package.
9. Open [signature_page_body_rules.md](signature_page_body_rules.md) to replace placeholders, resolve exceptions, apply language/capacity/seal/date rules, special-legend rules, fallback rules, and unsupported-value handling.
10. If the family is not listed in [signature_page_body_samples.md](signature_page_body_samples.md), use [signature_page_body_rules.md](signature_page_body_rules.md) fallback rules and record the unmatched file family in the task report or QA evidence. Do not use generic fallback to override a listed family or explicit variant.
11. Keep unsupported names, dates, titles, roles, seals, counts, or translations blank or flagged off-page. Do not guess on the page face.

## Sample And Rule Priority

`signature_page_body_samples.md` controls the body structure where a matching file family exists. For a listed family, the exact family/form/role variant controls the execution clause and any special signature legend. `signature_page_body_rules.md` controls variable replacement, exceptions, unmatched file families, and body points not directly covered by the sample.

If a desensitized sample and a general body rule conflict on structure for a matching file family, follow the sample structure and record the reason if the rule was adapted. If a non-body safeguard conflicts with body drafting convenience, keep the safeguard active.

For an unlisted family, retain the generic fallback process. Signing guidance may be used to identify that a file type and page scope must be handled, but the current transaction document determines the execution role, singular/plural choice, defined term, and special legend.

## Bundled Sample Status

The complete body samples are bundled in `signature_page_body_samples.md`. Use that file directly; no internal source document, screenshot, or previous project workspace is required to use this skill.

The desensitized SHA and SPA examples explain how one signing party can carry multiple investor identities and how its role placeholders are populated. They are structural explanations, not current-matter evidence.

Do not treat sample parties, signatories, projects, dates, or transaction facts as defaults for a new matter. Keep role placeholders in reusable examples and replace them in generated outputs only with current source-supported values. Use `Authorized Signatory` only when supported for the current matter.

## Complete Body Structure Rule

Do not split in-text headers, body blocks, and footers into separate reference files. Keep each sample as one complete body drafting block by file family. The three body references have separate functions:

- `signature_page_body_drafting.md`: entry point and drafting order.
- `signature_page_body_samples.md`: complete desensitized sample blocks.
- `signature_page_body_rules.md`: merged rules for variables, exceptions, fallback, and QA.

## Drafting Checklist

Before producing page bodies:

- Confirm each file's source decision.
- Confirm the party/file/count/signing-requirement matrices are complete enough for drafting.
- Confirm guidance, trackers, and file-piecing outputs have already been prepared from the matrices.
- Confirm the current document's title, defined term, execution clause, signature legends, signature roles, and page-specific execution role were read before sample selection.
- Confirm each signing party was validated from the current file itself; for SHA/SPA, confirm schedule group trace fields drive final capacity labels.
- Confirm the closest matching sample family was checked and either used or recorded as unavailable.
- Confirm the selected sample variant matches the current document family, form, execution role, singular/plural status, and special legend.
- Confirm the execution-clause subject matches the role stated in the current document.
- Confirm `has`/`have` agrees with the number and meaning of executing legal persons covered by the clause.
- Confirm the current document name or defined term is used where the sample requires it.
- Confirm `ACCEPTED AND AGREED:`, `AGREED AND ACCEPTED:`, `ACKNOWLEDGED AND AGREED:`, or another special legend is attached only to the correct Holder, Recipient, Accepting Party, or other countersigning role.
- Confirm no special legend replaces the required English `IN WITNESS WHEREOF` paragraph.
- Confirm all Chinese VIE-related samples remain Chinese only.
- Confirm sample placeholders are replaced only with current source-supported values.
- Confirm SHA/SPA body labels are not generic investor labels when the schedules provide specific groups, and are not hard-coded from investor short names.
- Confirm SHA/SPA desensitized examples in the sample library were used only to understand placeholder treatment, not as matter facts.
- Confirm no raw sample names, dates, transaction facts, or sample project details are used as defaults.
- Confirm the page body will not show source columns, source paths, generation basis, status labels, QA notes, or open questions.
- Confirm source traceability remains available in internal matrices, reports, manifests, and logs.
