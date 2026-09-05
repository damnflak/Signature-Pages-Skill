# Party And Signing Matrices

Use this reference to decide who signs what, how parties are grouped, and how many signature pages are needed.

## Required Matrices

Build these working tables before drafting outputs:

| Matrix | Minimum fields |
| --- | --- |
| Name matrix | Short name, full legal name, English name, Chinese name, original language, source_id, source_location, role, notes. |
| Investor grouping matrix | Investor, old/new/both status, latest-series involvement, prior-series involvement, Schedule A source, cap-table source, final group. |
| Company-side matrix | Founder, founder entity, group company, ESOP/reserve, director, officer, company, other role, document-specific signing entity, source. |
| File-party matrix | File number, folder group, short file name, full title, document language, signature-page source decision, signing party, party group, party role/capacity, source. |
| SHA/SPA schedule group trace matrix | file_name/file_id, signing_party, source_schedule_part, source_group_label_exact, source_party_text_or_quote, final_capacity_label_for_signature_page, source_locator, cap_table_cross_check_result, open_question_if_any. |
| Document count matrix | File number, folder group, short file name, document family, source-supported party/group count basis, file count, backup count, signature count, source, override note. |
| Signing-requirement matrix | Party, party type, document language, signer title/capacity wording, seal requirement, hand-sign requirement, witness/abstain/special requirement, source, open question. |

## Name And Group Rules

- Use short name, full legal name, English name, and Chinese name where available.
- Pull some party information from the cap table, but usually pull full legal names and investment series from SHA Schedules A and B.
- Do not use party short names, investor nicknames, or hard-coded name lists as capacity/group-label rules. Short names are for filenames and readable guidance only after the source-supported identity group is known.
- Classify investors as old investors or new investors by whether they invested before or in the newest series.
- If an investor appears both before and in the newest series, classify it as old investor.
- Use Schedule A for investors and investment series where available.
- Use Schedule B for company-side shareholders, including founders, founder entities, group companies, ESOP/reserve, and similar company-side parties.
- Under a shareholder or investor, track different signing entities and document-specific roles separately. For example, a director may sign director resolutions even if the same person or entity appears elsewhere as shareholder-related.
- Do not combine multiple signing parties into one signing-party cell, even if they appear on the same actual signature page.
- Chinese company names stay Chinese in Chinese pages, but English pages use a source-supported English translation name plus the Chinese original in parentheses. Do not invent translations.
- Chinese natural persons follow the same source-supported translation or romanization plus Chinese-original concept on English pages; mark an open question if support is missing.
- English company names stay English in both Chinese and English pages.
- Track Chinese-company seal requirements so drafting can add `(seal)` on English pages or `（盖章）` on Chinese pages.

## File-Party Matrix

Create a transaction-file-by-file signing-party matrix. Each row should represent one file-party relationship, not merely one file.

The current file controls whether a party signs that file. Cap-table records and other documents may help find candidates or conflicts, but they do not substitute for current-file support.

Required decision fields:

- File number from the source package, or assigned running number if none exists.
- File group from the source folder or legal family, such as main transaction documents, VIE/control documents, resolutions, ancillary documents, or other files.
- Short file name, using common abbreviations for long names where appropriate.
- Full document title and document language.
- Signature-page source decision: `existing_real_page`, `generate_from_sources`, `visual_reference_only`, or `open_question`.
- Each signing party, one party per row/cell.
- Party group: company side, old investor, new investor, director, founder, group company, ESOP/reserve, or other.
- Party role/capacity from the document, such as investor, shareholder, director, lender, borrower, principal, agent, company, warrant holder, or authorized signatory.
- Source locator for the current-file evidence that supports the file-party relationship, such as section, schedule, paragraph, execution clause, or signature block.
- For SHA pages, the schedule is the direct source for identity grouping. Add `source_schedule_part`, `source_group_label_exact`, `source_party_text_or_quote`, `final_capacity_label_for_signature_page`, `source_locator`, `cap_table_cross_check_result`, and `open_question_if_any`; preserve file-specific Schedule-supported series membership in detail, including multiple series where applicable.
- For SPA pages, the schedule is the direct source for identity grouping. Add the same SHA/SPA trace fields and state ODI or Non-ODI plus the current-round investment series from the SPA schedule where supported.
- For non-SHA/non-SPA files, capacity labels must come from that file's template, beginning text, signature block, or schedule; omit the label if no source support exists.
- Do not collapse detailed SHA/SPA labels into generic `Investor`, `Preferred Shareholder`, or similar labels when the schedule provides more specific groups.
- Do not draft capacity labels from `party_short_name`, filename text, or hard-coded investor-name rules.

## SHA/SPA Schedule Group Trace

For each SHA or SPA signing party, build a schedule group trace before drafting body pages:

| Field | Rule |
| --- | --- |
| `file_name` / `file_id` | Identify the SHA or SPA source file. |
| `signing_party` | One signing party per row, exactly as source-supported. |
| `source_schedule_part` | The schedule, exhibit, annex, or schedule subsection used. |
| `source_group_label_exact` | Exact group label from the schedule, preserving detailed labels and plus signs. |
| `source_party_text_or_quote` | Short source excerpt or text value tying the party to the group. |
| `final_capacity_label_for_signature_page` | Final label used on the page; derive from `source_group_label_exact` and source-supported drafting conventions, not from party short name. |
| `source_locator` | File and schedule/paragraph/table locator. |
| `cap_table_cross_check_result` | `match`, `conflict`, `missing_in_cap_table`, `not_checked`, or similar. This is auxiliary only. |
| `open_question_if_any` | Missing, conflicting, or legally uncertain grouping/capacity issue. |

Preserve multiple identities. If the SHA schedule shows Series Angel Preferred Shareholder, Series Angel+ Preferred Shareholder, Series A Preferred Shareholder, or other distinct groups for one party, carry all supported labels into the matrix and final capacity decision. If the SPA schedule shows ODI Investor, Non-ODI Investor, Series A Investor, or similar groups, preserve those labels instead of replacing them with a generic investor label.

Exact label examples to preserve when source-supported:

- SHA: `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:`
- SPA: `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:`

These labels are examples of final capacity labels generated from schedule trace fields. They do not designate any default signing party.

## Copy Counts And Signature Counts

- Build a document count matrix before naming signature-page outputs.
- Count visible file-copy/signature-count signals at the document level, not by hard-coding the same value on every page.
- Default document-level file count: count the source-supported signing parties or signing-party groups for that document, with company-side parties counted together as one party group where they sign as the same contract side.
- For investor-only guidance rows, each investor receives one copy of each transaction document to which it is a party/signatory unless the document count matrix or a source-supported override requires a family-level count.
- Allow file-copy count rules to be overridden by the cap table or separate user/source instruction, but record the source of the override in the document count matrix.
- Signature count equals the document-level file count plus one backup signature page in case a paper signature page is damaged, unless a source-supported override says otherwise.
- Signature-count fields in guidance, tracker outputs, and filenames must contain only numbers.
- If the source support is insufficient to compute a document-level count, leave an open question in the matrix instead of defaulting all outputs to `2`.

## Signing Requirements

Apply party-type rules, then override only when a source document says otherwise. Chinese-file signing requirements use Chinese wording; English-file signing requirements use English wording.

| Party type | Default requirement |
| --- | --- |
| Foreign company | Chinese files: `授权代表`; English files: `Authorized Signatory`. Usually identifiable by English-only names. Seal generally not required unless source says so. |
| Chinese limited company | Chinese files: `法人代表` plus company seal; English files: `Legal Representative` plus company seal. In English documents, use a source-supported English translation plus the Chinese original in parentheses; if no translation is supported, mark an open question. |
| Chinese limited partnership | Chinese files: `执行合伙人委派/授权代表` plus company seal; English files: `Managing Partner Appointed/Authorized Representative` plus company seal. |
| Natural person | Personal signature only; do not add a title/capacity field unless the source document requires a role-specific capacity. |
| Director signing as director | Director signature; title is usually `Director` for English director/board resolutions unless source says otherwise. |

Additional rules:

- In Chinese documents, Chinese company names remain Chinese and foreign company names remain English.
- In English documents, source-supported English translations for Chinese companies or natural persons should be followed by the Chinese original in parentheses; missing translation support is an open question, not a drafting license.
- Chinese companies require seal notation unless a source-supported exception applies: `(seal)` in English pages and `（盖章）` in Chinese pages.
- If a document expressly requires hand signing, record `Sign by hand` in signing requirements. Do not infer hand signing from document type alone.
- Preserve special requirements such as witness, abstention, board capacity, seal, date, or named signatory as separate fields and source them.
- Leave signer name blank in signature-page bodies unless the document expressly requires a name or the user provides it as an accepted input.
