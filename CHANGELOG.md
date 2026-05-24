# Changelog

All notable changes to this skill package will be documented in this file.

## [1.1.0] - 2026-05-24

### Changed

- Renamed runtime skill folder to `legal-financial-valuation-document-reviewer-assistant`.
- Removed nonstandard `compatibility` frontmatter from `SKILL.md`; compatibility now lives in `MANIFEST.md`.
- Rewrote trigger description to a concise `Use when...` form.
- Added formatting-only fast path.
- Added long-document handling.
- Added stop-loading guidance for references.
- Deduplicated approval, output, source verification, and final-output safety rules.
- Added multi-turn approved/rejected/pending state tracking.
- Added strict bracket notation: `{}` for formatting annotations only and `[]` for approved text changes only.
- Added purpose/load headers to references.
- Added visible-workings caveat for amount/calculation checks.
- Updated OpenAI and Claude metadata.
- Fixed mojibake in package files.

## [1.0.0] - 2026-05-24

### Added

- Initial release of `legal-financial-valuation-document-reviewer-assistant`.
- Added approval-controlled document review workflow.
- Added support for legal, financial, tax, audit, compliance, Chartered Accountant, Registered Valuer, and valuation documents.
- Added valuation report review instructions for ESOP, Rule 11UA, FEMA/RBI, Companies Act, IBBI, DCF, NAV, and option valuation contexts.
- Added Indian source-priority guidance for MCA, IBBI, Income Tax, ICAI, CBIC/GST, RBI, SEBI, and reputed professional sources.
- Added cross-border source map for Singapore, US, and UAE contexts.
- Added output format controls for Word-ready text, Markdown, annotated Markdown, change-marked Markdown, and DOCX-style workflows.
- Added detailed issue-by-issue review template.
- Added Claude-compatible portable prompt.
