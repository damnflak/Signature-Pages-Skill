# Guidance Trackers And Piecing

Use this reference to build lawyer-facing control documents from the same party and file matrices used for signature pages.

Prepare signing guidance, received trackers, and the file-piecing controlling list before drafting signature-page bodies. Final lawyer-facing tables should not include a source column; keep source IDs, source locations, status analysis, and traceability in internal matrices, reports, manifests, and logs.

The body sample library controls only signature-page body structure. It does not change tracker, guidance, piecing-list, source-traceability, or lawyer-facing table safeguards.

Table style defaults:

- Do not use MS Mincho.
- Default Chinese text to SimSun where available and English text to Times New Roman where available.
- Use Chinese table headers with blue fill for final delivery tables unless the user asks for a different style.
- Keep second-column groups and repeated third-column same party/file rows together; merge cells where practical.
- Do not repeat duplicate visible text inside merged display cells; show the merged value once while preserving underlying rows in internal matrices.
- Merge third-column cells where practical: if the table is organized by file, merge repeated file names; if organized by signing party, merge repeated signing parties.
- Use parentheses, not square brackets, for signing-party full names.
- Naturally short names do not need a repeated full name.
- Do not translate full legal names for delivery tables.
- Replace the word `plus` with `+` in series or label text where source meaning is plus.
- Signing-requirement wording follows document language: Chinese files use Chinese requirement wording and English files use English requirement wording. In Chinese-language delivery tables, keep English-file capacity labels in English and add Chinese action text only where needed for the table format, for example `Authorized Signatory签字`.
- For natural-person signing requirements, use personal-signature wording such as `本人签字` in Chinese-file/table contexts and do not add a company-role title unless source-supported.

## Investor-Side Signing Guidance

Format: DOCX/DOC.

Title: `Signing guidance` plus investor-side bracket text. Center the title. Use Chinese title and column labels when drafting the final lawyer-facing table.

Required columns:

| Column | Rule |
| --- | --- |
| `#No.` | One number per investor because the investor is the smallest sending unit. Keep the same first-column number for the same signing party. |
| Investor grouping | Old investors first, including investors that are both old and new, then new investors. Merge cells by group. |
| Signing parties | One party per cell. Place before the file-name column. Use short form plus original full name in parentheses when a full name is needed. Merge cells for the same company/natural person. Do not combine parties with plus signs. |
| Short file/doc name | Use short names or abbreviations. Keep file order consistent for each party where practical. |
| Signing requirements | Include signer and seal requirements. Add a second line `Sign by hand` only if expressly required. |
| Signature count | Numbers only. |

Language and naming for delivery tables:

- Preserve full legal names without translation in delivery tables: English names stay English and Chinese names stay Chinese.
- Each entity under the same investor shares that investor number.
- Do not break merged party-name cells merely to force exact file ordering.

## Company-Side Signing Guidance

Format: DOCX/DOC.

Organize by transaction document/file, not by investor.

Center the title. The file-name column should come before the signing-party column. The same file should share the same first-column number.

Required columns:

| Column | Rule |
| --- | --- |
| `#NO.` | Keep original file numbering. If none exists, assign 1, 2, 3, and so on. |
| File group | Derive from original transaction-document folder structure where practical, such as transaction docs, VIE/control files, resolutions, and other files. Merge group cells. |
| Short file name | Use short names and abbreviations. |
| Signing party | One name per cell, with short form plus full name in parentheses when a full name is needed. |
| Signing requirements | Same signer/seal/hand-sign rules as investor guidance. |
| Signature count | Numbers only. |

Common abbreviations:

- `SHA` for Shareholders Agreement.
- `SPA` for Subscription Agreement.
- `SR` for shareholder resolutions.
- `DR` for director resolutions.
- Keep already short names such as warrant or proxy directly.
- If multiple files share a name, prefix a distinguishable party or document signal, such as party name plus warrant or jurisdiction plus resolution.

## Received Trackers

Format: XLSX/XLS.

Create separate investor-side and company-side received trackers. Use the corresponding signing-guidance rows as the base so lawyers can track signature-page receipt without re-keying party decisions.

Required structure:

- Keep the guidance columns for number, group, file name, signing parties, signing requirements, and signature count.
- Add a blank `E-signature / scanned signature` tick/status column before signature count because scanned/e-signature pages are copyable.
- Add a blank `Paper copies` tick/status column after signature count because paper copies must match the required count.
- Make the last column `备注` and leave it blank for lawyer use by default.
- Preserve `received`, `missing`, `partial`, and `follow-up` status handling in internal matrices, QA reports, or annotated drafts if requested; do not prefill the final delivery tracker note column unless the user asks for annotations.
- Preserve separation between investor-side and company-side views.

## File-Piecing Controlling List

Format: XLSX/XLS.

Purpose: help lawyers assemble transaction documents and signature pages into complete files.

Organize by file like company-side signing guidance.

Required columns:

- Number.
- File group.
- File name.
- Signing parties.
- Signing requirements.
- File count.
- Signature count.
- Blank `备注` column where lawyer-facing notes are needed.

Ordering:

1. Company-side parties.
2. Old investors.
3. New investors.

Within each group, follow SHA or governing schedule order where available.

Keep both file-counting and signature-counting columns in the final workbook. Merge file-count and signature-count cells where practical for repeated signing-party rows under the same file.

## Matrix Consistency Rule

Signing guidance, received trackers, file-piecing lists, and signature-page filenames must be derived from the same underlying party/file/count matrices. Signature-page filename counts must use the document-level count matrix, while row-level guidance can show the applicable count for that party/document relationship. If any output differs from the matrix, record the override and source.

For SHA/SPA files, guidance, trackers, file-piecing lists, and signature-page bodies must use the same schedule group trace fields for identity and capacity labels. Do not substitute party short names, prior-output labels, or hard-coded investor-name rules for `source_group_label_exact` and `final_capacity_label_for_signature_page`.

Where SHA/SPA schedule trace fields support detailed combined labels, preserve the same exact label text across guidance, trackers, piecing lists, and page bodies. Do not shorten labels such as `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:` or `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:` into generic investor wording.
