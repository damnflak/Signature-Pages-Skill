# Signature Page Outputs

Use this reference to generate signature-page files after the source, party, and file matrices are complete.

For body-specific conflicts, including in-text headers, body templates, capacity/title wording, natural-person layouts, and English footers, use the three-file body architecture: `signature_page_body_drafting.md` as entry point, `signature_page_body_samples.md` as the direct sample source for matching file families, and `signature_page_body_rules.md` for variable replacement, exceptions, fallback, and body-specific QA. This reference controls output package structure, sequencing, file/folder organization, clean-page safeguards, and derivative production unless a body-specific rule is directly at issue.

## Output Package

Produce control materials before signature-page bodies: signing guidance, received trackers, and the file-piecing controlling list should be prepared from complete matrices before final page-body drafting. Produce editable DOCX/DOC signature-page outputs after those control materials, then derivative PDFs when requested or required. Keep editable files available for future legal manual edits.

Clean issued-page mode is the default for generated signature-page drafts unless the user expressly asks for annotated QA drafts.

Required output families:

- Old investor signature-page files in DOCX/DOC and PDF.
- New investor signature-page files in DOCX/DOC and PDF.
- Company-side signature-page files in DOCX/DOC and PDF.
- Investor-side signing guidance.
- Company-side signing guidance.
- Investor-side received tracker.
- Company-side received tracker.
- File-piecing controlling list.

These eight output families are required in this order for a complete package: old-investor signature pages, new-investor signature pages, company-side signature pages, investor-side signing guidance, company-side signing guidance, investor-side received tracker, company-side received tracker, and file-piecing controlling list.

## Folder Architecture And Names

Use the following naming patterns:

| Output | Folder and filename pattern |
| --- | --- |
| Old investors | `Old investors/#No-short form-full name/[short file name + signature count]signing party short name(s)_Project Name_Series X_Signature Pages` |
| New investors | Same pattern under `New investors`. Investors that are both old and new stay under old investors. |
| Company side | `Company side/File grouping/#No...`, preserving original file numbering where available. |

Rules:

- Use bracketed or clearly separated short file names where the package convention requires them.
- Separate multiple signing-party short names with commas in filenames when multiple parties are included in one generated file.
- Include project name and current/newest series in signature-page filenames where the naming pattern requires it.
- Use the source file number where one exists; otherwise assign stable running numbers.
- Do not import sample-specific folder names or dates from visual/reference materials unless the active source request independently supports them.
- Use the document-level signature count from the document count matrix in bracketed filename count signals. Do not reuse a uniform fallback count across unrelated document families.

## Clean Issued-Page Mode

Signature-page bodies must look like issued signature pages, not internal workpapers.

Presentation defaults:

- Do not use MS Mincho.
- Default Chinese text to SimSun where available.
- Default English text to Times New Roman where available.
- Record any local font fallback in the task report.

Do not place any of these on the signature-page face:

- Source path, folder path, or source ID.
- Source columns or other source-trace table fields.
- Generation basis or file-family explanation.
- Status labels such as generated-missing, draft, manifest, QA, received, missing, partial, or follow-up.
- Internal reviewer notes, package manifest details, confidence labels, or open-question text.

Keep those items in the source index, working matrices, package manifest, QA reports, execution logs, and other internal evidence. A page may still contain legal signing text, party/capacity labels, signature lines, name/title/date lines, seal notation, and the required English footer or Chinese no-text page header.

## English Signature-Page Pattern

English pages generally include an in-text header and a signature body.

Header:

- Begin with an `IN WITNESS WHEREOF` paragraph in capitals.
- Before selecting paragraph wording, identify the exact document family and the legal execution role covered by the current page.
- Use the file-family sample header from `signature_page_body_samples.md` when the document family provides one, and add one TAB as first-line indentation before the paragraph.
- For a family with multiple variants, use the exact family/form/role/singular-plural/special-legend variant in `signature_page_body_samples.md`.
- A special legend such as `ACCEPTED AND AGREED:`, `AGREED AND ACCEPTED:`, or `ACKNOWLEDGED AND AGREED:` is additional to, and does not replace, the `IN WITNESS WHEREOF` paragraph.
- If no corresponding family sample is found, use the fallback in `signature_page_body_rules.md` with the current file's full name inserted and record the unmatched family off-page.

Body sequence:

1. Any document-specific capacity label, role label, or special legend.
2. Party full legal name on a separate line from the role label.
3. Seal notation if a company needs a seal.
4. `By: _____________________`
5. `Name:` left blank unless expressly required.
6. `Title:` based on signing requirements and document language, such as `Authorized Signatory`, `Legal Representative`, `Managing Partner Appointed/Authorized Representative`, or `Director`; omit title for natural persons unless the source requires a role-specific capacity.
7. Date line only if the document type, source form, template, or user expressly requires it. If `Date:` appears, leave it blank without a long horizontal line.

English footer:

- Use a centered bottom footer in all capital letters: `SIGNATURE PAGE OF [FULL DOCUMENT NAME] OF [PROJECT COMPANY FULL LEGAL NAME]`.
- Use the document's full file name and the project-name company's full legal name, not short names, unless the source full legal name itself is short.

## Chinese Signature-Page Pattern

Chinese pages generally use a centered no-text signature-page header:

`[No text on this page; this is the signature page of ... (title at beginning of file)]`

Use the corresponding Chinese wording from the source drafting environment when producing final Chinese pages. Chinese signature pages have no footer.

Body sequence:

1. Party role label from the document if parties do not hold equal positions.
2. Party name or signer label.
3. Signature line.
4. Name/title line where required.
5. Company seal line where required.
6. Date line using the sample-style blank expression `年   月   日` where required.

## Document Family Drafting Patterns

Use `signature_page_body_samples.md` to select the signature body pattern. The table below is only an output-routing summary and must not replace the complete desensitized sample blocks.

| File family | Pattern |
| --- | --- |
| SHA | Use the mixed natural-person/entity SHA execution-clause sample; preserve schedule-supported investor/company group or series labels from the SHA schedule group trace matrix. |
| SPA | Use the mixed natural-person/entity SPA execution-clause sample; preserve SPA-schedule ODI/Non-ODI plus round/series labels from the SPA schedule group trace matrix. |
| MAA | Treat as no signature-page output when the file matrix records no signing party; do not invoke fallback merely because MAA is listed as a transaction document. This is not an English no-`IN WITNESS WHEREOF` exception because no English signature page is generated. |
| Disclosure Schedule | Use the disclosure schedule sample, including `COMPANY:` and `For and on behalf of ...` structure. |
| Warrant | Select joint Company/Holder company-page, joint Company/Holder holder countersignature-page, or issuer-only variant. |
| English shareholder resolutions | Select singular or plural Shareholder variant based on the number of shareholders covered by the execution clause. |
| English director/board resolutions | Select singular or plural Director variant based on the number of directors covered by the execution clause, and retain `Director` only where source-supported. |
| Chinese shareholder resolutions | Use the Chinese shareholder resolutions sample. For natural-person shareholders, do not add a title unless the source requires one. |
| Chinese director/board resolutions | Use the Chinese director/board resolutions sample, including company seal only where required. |
| Chinese VIE/control documents | Use only Chinese samples. Use the closest listed sample: exclusive service agreement, exclusive option agreement, voting rights proxy agreement, voting-rights-proxy POA, equity pledge agreement, equity-pledge POA, single status declaration, or loan agreement. Role labels must come from the document. Do not add English VIE samples. |
| Closing certificate | Use the closing certificate sample. |
| Director indemnification agreement | Use the director indemnification agreement sample. |
| Termination agreement | Use the ordinary termination agreement execution-clause sample and identify the current termination document by its defined term. |
| Termination agreement side letter | Use the `IN WITNESS WHEREOF` plus exact countersignature-legend sample. |
| Commitment letter | Select Promisor-only, multiple-Promisor, or Recipient/Accepting Party variant from the current document role and exact legend. |

## Generation Rules

- Generate only from source-supported parties and document families.
- Determine for each file whether to extract an existing real signature page, generate a missing page, use a visual reference only, or mark an open question before drafting. Confirm the specific signing parties from the current file itself.
- For SHA/SPA, generate capacity labels from the schedule group trace matrix fields `source_group_label_exact` and `final_capacity_label_for_signature_page`, not from party short names, filenames, or hard-coded investor-name rules.
- Preserve exact SHA/SPA label punctuation, slash-separated combined labels, and `+` signs where the schedule trace supports them, including labels such as `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:` and `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:`.
- Populate company and signatory placeholders only from current source support or an approved current-matter instruction. Do not select `Authorized Signatory` merely because it appears in a structural example.
- For non-SHA/non-SPA files, generate capacity labels only from the current file's beginning text, schedules, signature blocks, execution clauses, or source template.
- If a file family is not recognized, extract the source signature block pattern where available; otherwise use the fallback rules in `signature_page_body_rules.md` and mark the output as needing legal review.
- Keep special source formatting when it is material to signing, such as seal lines, hand-sign notes, witness lines, abstention lines, or named capacities.
- Keep generation of missing pages separate from extraction of real existing pages. Do not silently replace an existing page with a generated one.
- In clean issued-page mode, write unsupported signer names, dates, or titles as blanks only where the source does not support a final value; record the missing support off-page.

## Rerun And Prior-Output Safeguards

When rerunning a test or regenerating a package:

- Create a fresh output/work folder for the new round and preserve prior output folders as evidence.
- Rebuild the File-Party Matrix or equivalent source matrix from original transaction documents instead of reusing old output as the current source.
- Regenerate a SHA/SPA schedule group trace report when SHA/SPA files are in scope.
- Use old matrices and old outputs only as comparison baselines unless every reused row is revalidated against current original sources with a current source locator.
