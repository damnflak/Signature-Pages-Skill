# Signature Pages Skill

A Codex skill for preparing legal transaction signature-page packages from transaction documents and cap-table evidence.

## What it does

- Identifies signing parties and requirements from each transaction document.
- Preserves schedule-supported SHA/SPA capacity labels.
- Prepares signing guidance, receipt trackers, file-piecing lists, and signature-page bodies.
- Provides desensitized English and Chinese body samples with source-traceability and QA rules.

## Install

Copy the complete `signature-pages` folder into your Codex skills directory (normally `~/.codex/skills/`), then restart Codex. Keep `SKILL.md`, `agents/`, and `references/` together.

## Use

Invoke `$signature-pages` and provide your current transaction documents, cap table, and requested deliverables. Specify whether you need existing pages extracted or new pages drafted, and whether you need editable files, PDFs, signing guidance, or receipt trackers.

For example: "Use $signature-pages to prepare a signature-page package from the attached transaction documents and cap table. Include signing guidance, receipt trackers, and editable signature pages. Record missing evidence as open questions."

The skill contains instructions and sample structures; your working environment supplies the document, spreadsheet, and PDF tools. All bundled examples use role placeholders. No internal reference document or original client material is needed to use the skill. Current transaction documents determine parties, roles, names, and signing obligations; unsupported facts remain open questions. Review generated legal documents before use.

## Package

- `signature-pages/SKILL.md`: entry point and workflow.
- `signature-pages/agents/openai.yaml`: Codex discovery metadata.
- `signature-pages/references/`: nine supporting references and the complete body sample library.

Keep client documents, generated outputs, and working records outside this repository.
