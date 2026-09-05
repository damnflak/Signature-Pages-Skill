# QA And Testing

Use this reference to check a generated or extracted signature-page package. Keep task-specific test reports outside the skill folder.

## Completeness Checks

Before delivery or handoff, confirm that the package includes all requested output families:

- Old investor signature-page files in editable format and PDF when requested.
- New investor signature-page files in editable format and PDF when requested.
- Company-side signature-page files in editable format and PDF when requested.
- Investor-side signing guidance.
- Company-side signing guidance.
- Investor-side received tracker.
- Company-side received tracker.
- File-piecing controlling list.

Confirm every output row or file traces back to the party/file/count matrices.

Confirm the workflow order: complete matrices first, then signing guidance, received trackers, and file-piecing list, then signature-page bodies last.

Confirm body-reference architecture: `signature_page_body_drafting.md`, `signature_page_body_samples.md`, and `signature_page_body_rules.md` exist, are directly linked from `SKILL.md`, and preserve the sample-first body drafting relationship. Matching file families must use the desensitized sample library as the direct body structure; general body rules replace variables, resolve exceptions, and handle unmatched families. General workflow, source, output-package, tracker, QA, PDF derivative, traceability, sample-leakage, and legal-review rules must remain active.

Confirm body-header architecture: before selecting a body sample, the drafter identifies the current document family, document form, execution role, special legend, and number of executing legal persons covered by the clause. Listed families must use the exact family/form/role/singular-plural/special-legend variant; unlisted families keep generic fallback.

Confirm desensitized body-example architecture: SHA/SPA samples contain role placeholders and population notes, preserve exact SHA/SPA labels where source-supported, and do not include real sample parties or signatories.

## Matrix QA

Check these before using the matrices for final outputs:

- Every signing party has a source locator.
- Every file-party relationship has a source locator.
- Every file-party relationship is supported by the current file itself. Cap-table rows and other files may be cross-checks, but not substitutes for current-file support.
- SHA/SPA signer identity groups are traced to schedules with `source_schedule_part`, `source_group_label_exact`, `source_party_text_or_quote`, `final_capacity_label_for_signature_page`, `source_locator`, `cap_table_cross_check_result`, and `open_question_if_any`.
- SHA/SPA final page capacity labels read from the schedule group trace matrix, not from `party_short_name`, filename text, or hard-coded investor-name rules.
- Prior matrices or prior outputs used during a rerun were revalidated row by row against current original source files, or were kept only as comparison baselines.
- Every signature count is numeric and ties to the document count matrix unless a source-supported override exists.
- Company-side parties are counted together as one party unless a source-supported override exists.
- Investors that are both old and new are grouped with old investors.
- SAFE, warrants, and similar shareholder-like rights were reviewed for party discovery without being automatically turned into signatories.
- Hand-sign requirements appear only when a source expressly supports them.
- Chinese company and limited partnership seal/signature rules are applied or marked as open questions when party type is uncertain.
- Signing requirements use Chinese wording for Chinese files and English wording for English files.
- Chinese company and natural-person English-page display names use source-supported English translation/romanization plus Chinese original in parentheses, or are marked as open questions.
- Natural-person body/title rules omit title fields unless the source requires a role-specific capacity such as director.
- Multi-party actual signature pages do not cause multiple signing parties to be collapsed into one tracker cell.

## Source Traceability QA

- Material party, series, count, signing requirement, document-family, and output naming decisions have source IDs and source locations.
- Missing full names, missing source locations, conflicting schedules, unclear party type, unclear series, and uncertain legal roles remain visible as open questions.
- Existing signature pages, if used, are classified as extracted source pages or visual/reference pages rather than silently treated as drafting rules.
- Cap-table evidence is classified as auxiliary cross-check evidence for file-specific obligations, not as the source that creates a signing obligation.
- Issued-page signature bodies contain no source paths, generation-basis text, status labels, manifest references, QA notes, or other internal traceability metadata.
- Source traceability remains available off-page in source indexes, working matrices, manifests, reports, and logs.
- Final lawyer-facing delivery tables do not include a source column unless the user expressly asks for annotated drafts.

## Sample-Leakage QA

Before treating a rule as reusable, ask whether it comes from:

1. The active user request or approved instructions.
2. The source transaction documents/cap table for the current matter.
3. A sample folder, visual reference, or prior package.

Do not encode sample-specific names, dates, folder notes, file names, or transaction facts as reusable rules unless the active source request independently supports them.

Approved desensitized body samples are the exception for structure only: preserve their full body structure by file family, but replace all sample-specific parties, names, projects, dates, titles, and transaction facts with placeholders or current source-supported values.

## Body Sample Coverage QA

For every generated body:

- Confirm `signature_page_body_samples.md` was checked for the closest matching file family.
- Confirm every requested document family is matched to a bundled sample in `signature_page_body_samples.md`, or the task report records the unmatched family and fallback used.
- Confirm matching families use the sample structure rather than a generic body template.
- Confirm the sample block preserves in-text header, body sequence, signature block, date/seal treatment, and footer pattern where applicable.
- Confirm every generated English signature page starts with `IN WITNESS WHEREOF`, except no-output routes where no page is generated.
- Confirm special legends such as `ACCEPTED AND AGREED:`, `AGREED AND ACCEPTED:`, and `ACKNOWLEDGED AND AGREED:` are exact, role-specific, and additional to the `IN WITNESS WHEREOF` paragraph.
- Confirm signing-party role labels and signing-party names are on separate lines in signature blocks.
- Confirm fallback uses `has` for one executing legal person and `have` for two or more executing legal persons, based on the clause meaning rather than the number of visible signature blocks on one page.
- Confirm SHA and SPA execution clauses use `each Party has executed this Agreement or caused this Agreement to be executed on its behalf`.
- Confirm SHA and SPA capacity labels preserve exact schedule-supported group detail and are not compressed into generic investor or preferred-shareholder labels.
- Confirm SHA and SPA desensitized-example population notes are present for grouping, signing party, `By:`, `Name:`, and `Title:` lines.
- Confirm the exact SHA label `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:` and exact SPA label `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:` are available as examples and not altered.
- Confirm MAA with no signing party is no-output and does not invoke fallback.
- Confirm Warrant output selects the joint Company/Holder company page, joint Company/Holder holder page, or issuer-only variant from the current document.
- Confirm English shareholder and director/board resolutions use `has executed` or `have executed`, not `has caused`.
- Confirm Chinese VIE, POA, equity pledge, and single-status declaration samples remain Chinese-only.
- Confirm Termination Agreement, Termination Agreement Side Letter, and Commitment Letter pages use the current document defined term and exact countersignature/acceptance legend where applicable.
- Confirm sample placeholders were replaced only with current source-supported values.
- Confirm no raw sample company names, natural-person names, project names, investor names, dates, or transaction facts appear as defaults.
- Confirm unmatched file families are recorded with the fallback rule used and legal-review limitation.

## Visual-Reference-Only QA

When the user provides unsigned issued signature pages or another reference package for visual comparison:

- Use the reference only after generating from source transaction documents.
- Compare layout, naming, party grouping, copy-count signals, signing-guide presence, and obvious completeness.
- Do not use the visual reference to replace extraction from transaction documents or cap tables.
- Record differences as pass/fail observations or rework candidates tied to source-backed requirements.

## Received/Missing/Partial QA

When tracking signature-page status:

- Mark pages or rows as `received`, `missing`, `partial`, or `follow-up` where the task includes status tracking.
- Keep e-signature/scanned receipt separate from paper-copy receipt.
- Do not treat one scanned/e-signature receipt as satisfying required paper copy counts.
- Preserve extracted real pages separately from generated missing pages.

## Package Review

Review final package organization:

- Folder names match old investor, new investor, and company-side grouping.
- Filenames include the required short file, count, party, project, series, and signature-page signals where applicable.
- Filename count signals reconcile to the document-level count matrix and are not uniformly defaulted across all documents.
- Editable files are present where future manual edits are expected.
- PDFs are derivative of the editable files when PDFs are requested.
- Outputs do not use MS Mincho; Chinese defaults to SimSun and English defaults to Times New Roman where available, with fallback noted in the report.
- English in-text headers use the body-sample family wording where available and have one TAB first-line indentation before `IN WITNESS WHEREOF`.
- Special-format legends do not replace the English `IN WITNESS WHEREOF` paragraph and are not swapped across `ACCEPTED AND AGREED`, `AGREED AND ACCEPTED`, or `ACKNOWLEDGED AND AGREED` word orders.
- Signature-page role labels and signing-party names appear on separate lines.
- English pages have all-capital footers using the full document name and project-name company full legal name; Chinese pages have no footer.
- English page bodies do not include dates unless expressly required, and any `Date:` value is blank without a long line.
- Chinese page bodies use the sample-style blank date expression `年   月   日` where a date line is required.
- Guidance, trackers, and file-piecing list all reconcile to the same underlying matrices.
- Signing guidance titles are centered.
- Investor-side guidance is organized by signing party, with the signing-party column before the file-name column and the same party sharing the same first-column number.
- Company-side guidance is organized by file, with the file-name column before the signing-party column and the same file sharing the same first-column number.
- Final trackers use a blank last column named `备注`.
- File-piecing lists retain both file-counting and signature-counting columns.
- Merged guidance-table cells do not repeat duplicate visible text.
- Third-column cells are merged where practical according to organization mode: file-first tables merge file names, and party-first tables merge signing parties.

## Body Variant Acceptance Checks

When checking body variants, report PASS/FAIL for these focused checks:

1. SHA mixed parties: execution clause uses `each Party has executed ... or caused ... to be executed on its behalf`.
2. SPA mixed parties: same mixed natural-person/entity clause behavior as SHA.
3. English house style: every generated English page begins with `IN WITNESS WHEREOF`.
4. Generic fallback: unlisted English families still use fallback; one executing legal person uses `has`, two or more use `have`.
5. MAA: if the file matrix has no signing party, no signature page is generated and fallback is not invoked.
6. Joint Warrant company page: clause states the Company and Holder have executed the Warrant and shows the Company block.
7. Joint Warrant holder page: repeats the company-page `IN WITNESS WHEREOF`, preserves the exact holder legend, and places the Holder block under that legend.
8. Issuer-only Warrant: clause states the Company has caused the Warrant to be duly executed and has no Holder legend.
9. English shareholder resolutions singular: uses `Shareholder has executed these resolutions` and not `has caused`.
10. English shareholder resolutions plural: uses `Shareholders have executed these resolutions`.
11. English director/board resolutions singular: uses `Director has executed these resolutions` and not `has caused`.
12. English director/board resolutions plural: uses `Directors have executed these resolutions`.
13. Chinese VIE-only scope: newly listed VIE, POA, equity pledge, and single-status declaration samples remain Chinese only.
14. Equity Pledge Agreement header: uses the dedicated Chinese equity-pledge no-text header.
15. Two POA headers: voting-rights-proxy POA and equity-pledge POA use distinct source-agreement headers.
16. Single Status Declaration: uses the Chinese declaration sample and has no English declaration sample.
17. Ordinary Termination Agreement: execution clause identifies the current termination document, not a bare `this Agreement`.
18. Termination Agreement Side Letter: every page keeps `IN WITNESS WHEREOF`; accepting pages use the exact `AGREED AND ACCEPTED`-type legend.
19. Commitment Letter Promisor: Promisor appears in the primary signing block, not under `ACCEPTED AND AGREED:`.
20. Commitment Letter Recipient: only the actual accepting party appears below the exact countersignature legend, while the page still keeps the document-level `IN WITNESS WHEREOF`.
21. Legend preservation: `ACCEPTED AND AGREED`, `AGREED AND ACCEPTED`, and `ACKNOWLEDGED AND AGREED` are not swapped.
22. No collateral changes: footer, name/signature/title rules, seal/witness/date rules, Chinese/English name rules, output package architecture, and unlisted samples remain unchanged except where a specific body-variant rule says otherwise.

## Source And Schedule Acceptance Checks

When checking source and schedule handling, report PASS/FAIL or open-question status for these focused checks:

1. Each file's signing parties are confirmed from the current file itself, with locators to parties, preamble, recitals, definitions, schedules, signature blocks, execution clauses, or equivalent source locations.
2. Cap-table evidence is used only for discovery, consistency checks, and open-question creation; it does not create a file-specific signing obligation.
3. SHA/SPA schedules are used as the direct drafting source for signer identity grouping.
4. The SHA/SPA schedule group trace matrix includes `file_name`/`file_id`, `signing_party`, `source_schedule_part`, `source_group_label_exact`, `source_party_text_or_quote`, `final_capacity_label_for_signature_page`, `source_locator`, `cap_table_cross_check_result`, and `open_question_if_any`.
5. SHA labels preserve detailed groups, including multiple groups where the source supports them, and are not collapsed into generic `Preferred Shareholder` or `Investor` labels.
6. SPA labels preserve ODI/Non-ODI and series labels where the source supports them, and are not collapsed into generic `Investor` labels.
7. Signature-page capacity labels are driven by `source_group_label_exact` and `final_capacity_label_for_signature_page`, not by party short names or hard-coded investor-name rules.
8. Non-SHA/non-SPA files use current-file evidence for signer and capacity decisions; unresolved items are recorded as open questions.
9. Old output packages and old working matrices are not used as current source unless every reused row was revalidated against current original source files.
10. Fresh rerun output and working evidence are written to a new folder without overwriting prior test-output folders.
11. The generated File-Party Matrix or equivalent source matrix lists signing party and source locator file by file.
12. Reviewer evidence checks per-file sources, SHA/SPA group preservation, Cap Table auxiliary-only use, old-matrix reuse, hard-coded labels, skill validation, and any checks provided by the active workspace.

## Desensitized Example Acceptance Checks

When checking desensitized examples, report PASS/FAIL or open-question status for these focused checks:

1. `signature_page_body_drafting.md` remains the mandatory entry point for body drafting.
2. `signature_page_body_samples.md` remains the matching-family structure source and now contains desensitized-example population notes for SHA and SPA.
3. `signature_page_body_rules.md` remains the variable/exception/fallback/leakage rule source and states that desensitized examples are not current-matter evidence.
4. The SHA example preserves `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:` exactly.
5. The SPA example preserves `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:` exactly.
6. Reusable SHA and SPA examples contain `[SIGNING PARTY FULL LEGAL NAME]` rather than a real company or client name; generated names require current source support.
7. Reusable SHA and SPA examples contain `[AUTHORIZED SIGNATORY NAME]` rather than a real person's name; generated names require current source support.
8. `Authorized Signatory` appears only as a structural example title or a current source-supported title/capacity.
9. Company-side examples use role placeholders and the bundled body structure, without requiring an internal screenshot or supplying default company-side facts.
10. SHA/SPA generated capacity labels remain driven by `source_group_label_exact` and `final_capacity_label_for_signature_page`.
11. Cap-table evidence remains auxiliary only and does not create signing obligations.
12. Existing source-boundary, output package, QA, tracker/piecing, traceability-off-page, PDF derivative, sample-leakage, and legal-review safeguards remain active.
