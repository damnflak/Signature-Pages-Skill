# Signature Page Body Rules

Use this file with `signature_page_body_drafting.md` and `signature_page_body_samples.md`. The sample library controls body structure for matching file families; these rules control variables, exceptions, fallback behavior, and QA.

## Source Decision Before Drafting

For each transaction file, record a source decision before drafting:

| Decision | Use when | Drafting result |
| --- | --- | --- |
| `existing_real_page` | The source transaction file already contains a real signature page. | Extract the page directly and preserve provenance. Do not generate a substitute unless separately instructed. |
| `generate_from_sources` | A page must be separately prepared. | Generate from transaction documents and auxiliary cross-check evidence, with transaction documents controlling file-specific signing obligations. |
| `visual_reference_only` | The user provides issued pages or samples only for visual comparison. | Use them after source-based generation for layout/QA only. |
| `open_question` | The source does not support the page source, signer, role, count, translation, or seal rule. | Record an off-page open question and do not guess. |

Confirm the specific signing parties file by file from the current file itself before using this table. For non-SHA/non-SPA files, do not fill a missing signer or capacity from the cap table or a different transaction document. For SHA/SPA files, use schedules as the direct drafting source for identity group labels and retain the schedule locator.

## Sample Priority

- First search `signature_page_body_samples.md` for the closest file family.
- When a matching sample family exists, select the exact family, document form, execution role, singular/plural, and special-legend variant, then copy its complete structure as the body drafting base.
- Replace only placeholders supported by the current transaction documents, schedules, cap table, or user-approved instructions.
- Use these rules for variable replacement, exceptions, and points the sample does not cover.
- Use fallback rules only when no matching sample family exists or the source document has a materially different signature block.
- Do not use generic fallback to override a listed family or explicit variant. Signing guidance can identify page scope, but the current transaction document controls execution role, defined term, singular/plural choice, and special legend.

## Desensitization And Variable Replacement

Replace sample facts with current source-supported values. Required placeholder treatment includes:

- Specific company names -> `[SIGNING PARTY FULL LEGAL NAME]`, `[PROJECT COMPANY FULL LEGAL NAME]`, or `[TARGET COMPANY]`.
- Current document defined term -> `[DOCUMENT DEFINED TERM]`.
- Warrant holder term -> `[HOLDER DEFINED TERM]`.
- Exact countersignature, acceptance, or acknowledgment legend -> `[COUNTERSIGNATURE LEGEND]`.
- Commitment-letter promisor or commitment-party term -> `[PROMISOR DEFINED TERM]`.
- Commitment-letter recipient or accepting-party term -> `[RECIPIENT DEFINED TERM]`.
- Specific natural-person names -> `[AUTHORIZED SIGNATORY NAME]`, `[NATURAL PERSON NAME]`, or `[CHINESE ORIGINAL NAME]`.
- Specific project, investor, shareholder, signing-party, or transaction names -> source-supported placeholders.
- Specific dates -> blank date line or `[DATE]` only when the source supports a value.
- File titles containing sample project or party names -> `[DOCUMENT FULL NAME]` or the current document title.
- Any fact obviously belonging only to a sample transaction -> remove as a fact and keep only the structure.

Bundled examples use role placeholders to explain variable replacement. Keep real company, client, project, and natural-person names out of reusable skill content. Apply the following treatment to generated outputs:

| Placeholder or example field | Reusable treatment |
| --- | --- |
| Signing-party name | Populate `[SIGNING PARTY FULL LEGAL NAME]` with the current signing party's source-supported full legal name. |
| Named signatory | Populate `[AUTHORIZED SIGNATORY NAME]` only where a named signatory is source-supported; otherwise leave `Name:` blank. |
| Project or company name | Populate `[SIGNING PARTY FULL LEGAL NAME]`, `[PROJECT COMPANY FULL LEGAL NAME]`, or `[TARGET COMPANY]` from the current source, according to the role. |
| `Authorized Signatory` | Use only where the signing-requirement matrix supports that capacity/title for the current party and document language. |

Do not desensitize or delete reusable structural content such as `IN WITNESS WHEREOF`, Chinese no-text page headers, `By:`, `Name:`, `Title:`, `签字：`, `姓名：`, `职务：`, `日期： 年  月  日`, `(seal)`, `（盖章）`, capacity-label structure, body sequence, or footer format.

## In-Text Header Rules

- English pages use the matching sample `IN WITNESS WHEREOF` header where available.
- Add one TAB as first-line indentation before the English `IN WITNESS WHEREOF` paragraph.
- Do not delete `IN WITNESS WHEREOF`, create an English no-`IN WITNESS WHEREOF` variant, or let a special legend replace the `IN WITNESS WHEREOF` paragraph.
- Chinese pages use a centered no-text header in the pattern `【本页无正文，为...的签署页】`.
- Use the current document title and target/project company from source evidence. Do not import sample titles or company names.

If no sample family matches, use this English fallback with the current full document name:

```text
	IN WITNESS WHEREOF, the undersigned [has/have] executed and delivered this [DOCUMENT FULL NAME] as of the date first written above.
```

Use `has` when the clause covers one executing legal person. Use `have` when the clause covers two or more executing legal persons. Do not choose `has` merely because the current page has one visible signature block; read the current document to determine what `the undersigned` covers.

## Execution Clause Subject Rules

Choose the `IN WITNESS WHEREOF` subject from the current document's family, defined terms, execution role, and number of executing persons:

| Current document situation | Subject / clause direction |
| --- | --- |
| Ordinary multi-party agreement | Use `each Party` or `the Parties` as supported by the sample and document. |
| Issuer-only Warrant | Use `the Company` or source-defined issuer term. |
| Joint Company-and-Holder Warrant | Use `the Company and the [HOLDER DEFINED TERM]`. |
| One Shareholder signing written resolutions | Use `the undersigned Shareholder`. |
| Multiple Shareholders covered by one execution clause | Use `the undersigned Shareholders`. |
| One Director signing written resolutions | Use `the undersigned Director`. |
| Multiple Directors covered by one execution clause | Use `the undersigned Directors`. |
| One principal signing a Chinese POA | Use the dedicated Chinese no-text header, not an English execution clause. |
| One declarant signing a Chinese Single Status Declaration | Use the dedicated Chinese no-text header, not an English execution clause. |
| Ordinary Termination Agreement | Use `the Parties` and the current termination document's defined term. |
| Termination Agreement Side Letter | Use the parties or exact role wording in the document plus any applicable countersignature legend. |
| One Commitment Party / Promisor | Use the source-defined singular `Promisor` or `Commitment Party` term. |
| Multiple Commitment Parties / Promisors | Use the source-defined plural `Promisors` or `Commitment Parties` term. |

Do not use these known-bad substitutions:

- `each Party have`.
- `the undersigned have` when the clause covers one person.
- `the undersigned has` when the clause covers multiple persons.
- A natural-person party `has caused` a duly authorized representative to execute.
- `the parties hereto` for an issuer-only Warrant.
- Bare `this Agreement` when the current sample must identify `this Termination Agreement`, `this Side Letter`, `this Warrant`, or another current document defined term.

## Special-Format Legends

Special legends are role-specific countersignature, acceptance, or acknowledgment legends. Examples include:

```text
ACCEPTED AND AGREED:
AGREED AND ACCEPTED:
ACKNOWLEDGED AND AGREED:
ACCEPTED AND AGREED TO:
AGREED AND ACCEPTED AS OF [DATE]:
```

Rules:

- Keep `IN WITNESS WHEREOF` at the beginning of each generated English signature page.
- Place the special legend before the signature block of the party that actually countersigns, accepts, acknowledges, or agrees in that role.
- Do not place the main promisor, issuer, ordinary contracting party, or commitment party under `ACCEPTED AND AGREED:` unless the current document expressly assigns that accepting role.
- Use a Holder, Recipient, Accepting Party, or similar role under a special legend only when the current document makes that party a countersigning, accepting, or acknowledging party.
- Preserve the exact legend wording and word order from the current document. Do not swap `AGREED AND ACCEPTED`, `ACCEPTED AND AGREED`, or `ACKNOWLEDGED AND AGREED`; do not remove dates or limited-purpose wording embedded in the legend.
- If a complete file has multiple signature pages, each page uses the same document-level `IN WITNESS WHEREOF` clause, with the special legend added only on the page bearing that role.

## Role Label And Party Name Layout

Keep any role label or capacity label on its own line, followed by the signing-party full legal name on the next line. Do not combine them on one line.

Correct pattern:

```text
[SOURCE-SUPPORTED ROLE LABEL]:
[SIGNING PARTY FULL LEGAL NAME]
```

Incorrect pattern:

```text
[SOURCE-SUPPORTED ROLE LABEL]: [SIGNING PARTY FULL LEGAL NAME]
```

## Date Rules

- English signature-page bodies should not include a date line unless the source document, template, or user expressly requires it.
- If `Date:` appears in an English page, leave the value blank unless the source supports a final date. Do not add a long horizontal line after it.
- Chinese signature-page bodies should include the sample-style blank date expression where a date line is required: `日期： 年  月  日`.
- Unsupported final dates stay blank and are recorded off-page.

## Capacity, Title, And Party Labels

Use the document language and party type to choose signing-requirement and body title/capacity wording.

| Party type | Chinese-file body title/capacity | English-file body title/capacity |
| --- | --- | --- |
| Foreign company | `授权代表` | `Authorized Signatory` |
| Chinese limited company | `法人代表` | `Legal Representative` |
| Chinese limited partnership | `执行合伙人委派/授权代表` plus seal requirement unless a source-supported exception applies | `Managing Partner Appointed/Authorized Representative` plus seal requirement unless a source-supported exception applies |
| Natural person | No title/capacity field by default | No title/capacity field by default |
| Natural person signing in a source-required role, such as director | Use the source-required role wording | Use the source-required role wording, such as `Director` |

For SHA:

- Use the SHA schedule group trace matrix to state the file-specific investor group or company group before the party name.
- Read `source_group_label_exact` and `final_capacity_label_for_signature_page`; do not derive the label from `party_short_name`, filename text, or hard-coded investor names.
- State applicable series in detail, including multiple series where applicable, and do not compress detailed labels into generic `Preferred Shareholder` or `Investor` wording.
- Exact preservation example: if the schedule supports a single party in Series Angel, Series Angel+, and Series A capacities, the final label may need to preserve `THE SERIES ANGEL PREFERRED SHAREHOLDER/ THE SERIES ANGEL+ PREFERRED SHAREHOLDER/ THE SERIES A PREFERRED SHAREHOLDER:` exactly.
- Example structure only:

```text
[SERIES / GROUP LABEL]:
[SIGNING PARTY FULL LEGAL NAME]
```

For SPA:

- Signing investors are current-round investors unless the source says otherwise.
- Use the SPA schedule group trace matrix to state ODI or Non-ODI plus the investment round or series.
- Read `source_group_label_exact` and `final_capacity_label_for_signature_page`; do not derive the label from `party_short_name`, filename text, or hard-coded investor names.
- Do not compress detailed ODI/Non-ODI/series labels into generic `Investor` wording.
- Exact preservation example: if the schedule supports a Non-ODI current-round Series A investor, the final label may need to preserve `THE NON-ODI INVESTOR/ THE SERIES A INVESTOR:` exactly.
- Example structure only:

```text
[ODI / NON-ODI AND SERIES LABEL]:
[SIGNING PARTY FULL LEGAL NAME]
```

For other files:

- Follow the source template and the signing party's specific role in that file.
- Prefer roles extracted from the beginning of the document, signature blocks, or schedules.
- If no source-supported role is found, omit the capacity label rather than inventing one.

## Natural-Person Body Patterns

For natural-person signing parties, generally do not add title or company-role fields. A title reflects a role in a company and should appear only when the source document requires the natural person to sign in that capacity, such as director in director/board resolutions.

Chinese natural-person structure:

```text
[NATURAL PERSON NAME]
签字：___________________
日期： 年  月  日
```

English natural-person structure:

```text
By: _____________________________
Name: [source-supported English or romanized name] ([Chinese original if source-supported])
```

Do not invent romanized names or translations. If source support is missing, mark an off-page open question.

## Name Language And Seal Rules

- Chinese company names stay Chinese on Chinese pages.
- On English pages, a Chinese company should use its source-supported English translation plus the Chinese original in parentheses. If no translation is source-supported, mark an open question rather than inventing one.
- Chinese natural persons follow the same concept: use a source-supported English or romanized name plus the Chinese original in parentheses on English pages when available; otherwise mark an open question.
- English company names stay English on both Chinese and English pages.
- Chinese companies require a seal unless a source-supported exception applies.
- After a Chinese company name, add `(seal)` on English pages or `（盖章）` on Chinese pages.

## English Footer

Use all capital letters in the centered English footer. Use the full document name and end with the project-name company's full legal name:

```text
SIGNATURE PAGE OF [DOCUMENT FULL NAME] OF [PROJECT COMPANY FULL LEGAL NAME]
```

Do not use a short file name or short project name unless the source full legal name itself is short. Chinese pages have no footer unless a source-specific Chinese form requires one.

## Fallback For Unmatched File Families

If no matching file family exists in `signature_page_body_samples.md`:

1. Extract the source signature block pattern if the transaction document has one.
2. If the source has no usable block, use the generic English or Chinese header/body structure closest to the document language.
3. For English fallback, select `has` or `have` by the number and meaning of executing legal persons covered by the clause.
4. Keep unsupported signer names, titles, dates, and translations blank.
5. Record the unmatched file family, selected fallback, and open questions in QA evidence or the task report.
6. Mark the output as needing legal review.

## Body-Specific QA

Before handoff:

- Confirm the closest matching sample was checked for every generated body.
- Confirm every matching family used the sample structure rather than a generic body template.
- Confirm in-text header, body sequence, signature block, date/seal treatment, and footer pattern match the selected sample unless a source-supported exception is recorded.
- Confirm every generated English page begins with `IN WITNESS WHEREOF`, except no-output routes such as MAA where no signature page is generated.
- Confirm special legends are exact, role-specific, and additional to `IN WITNESS WHEREOF`.
- Confirm role labels and signing-party names are on separate lines.
- Confirm execution-clause subjects and `has`/`have` choices match the current document role and number of executing persons.
- Confirm SHA/SPA mixed natural-person/entity pages use `each Party has executed ... or caused ... to be executed on its behalf`.
- Confirm Warrant pages use the correct joint Company/Holder or issuer-only variant.
- Confirm English shareholder and director/board resolutions use `has executed` or `have executed`, not `has caused`.
- Confirm Termination Agreement, side-letter, and Commitment Letter pages use the current document defined term and correct accepting/recipient/promisor role.
- Confirm Chinese VIE, POA, equity-pledge, and single-status declaration additions remain Chinese only.
- Confirm all placeholders were replaced only with current source-supported values.
- Confirm raw sample names, dates, transaction facts, and sample project details do not appear on page faces or in reusable rules.
- Confirm SHA/SPA capacity labels on page faces are driven by `source_group_label_exact` and `final_capacity_label_for_signature_page`, with source locators preserved off-page.
- Confirm unsupported sample-specific values are absent from generated page faces unless the current source independently supports them.
- Confirm non-SHA/non-SPA capacity labels come from the current file, not from the cap table or another file.
- Confirm body drafting did not weaken tracker, piecing list, source traceability, QA, PDF derivative, sample-leakage, output-package, or legal-review safeguards.
