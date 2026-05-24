# File Manifest

This manifest explains every file included in the skill package.

## Compatibility

- Web search: required for source verification. If unavailable, the skill should flag references for manual verification instead of claiming verification.
- `docx` skill: required for actual `.docx` output. If unavailable, the skill should offer Word-ready text or Markdown instead.
- Reduced-capability mode: the skill can still review, format, and prepare Word-ready or Markdown output without web search or `docx`.
- Runtime frontmatter: `SKILL.md` intentionally contains only `name` and `description`; compatibility details are package documentation, not trigger metadata.

## Root Files

### `SKILL.md`

Primary skill entrypoint. Contains YAML frontmatter, concise trigger description, core gates, progressive loading map, fast path, long document handling, dependencies, workflow pointer, and final output safety rule.

### `README.md`

User-facing documentation explaining purpose, workflow, key capabilities, compatibility, and strict bracket notation.

### `MANIFEST.md`

This file. Lists bundled files, compatibility expectations, and each file's purpose.

### `CHANGELOG.md`

Package change history.

### `LICENSE`

License file.

## Configuration

### `agents/openai.yaml`

OpenAI/Codex UI metadata. Defines display name, short description, default prompt, and brand color.

### `agents/claude.yaml`

Claude-oriented UI metadata plus declared dependency notes.

## Reference Files

### `references/01-review-workflow.md`

End-to-end review workflow for intake, document classification, file routing, issue review, approval gates, table conversion gate, output format gate, final formatting, and change summary.

### `references/02-approval-and-gating.md`

Canonical approval rules defining what counts as a text change, required approval gates, approval options, ambiguous approval handling, and multi-turn approved/rejected/pending state.

### `references/03-output-formats-and-change-marking.md`

Canonical output format rules for Word-ready text, Markdown, formatting annotations using `{}`, change-marked Markdown using `[]`, DOCX fallback behavior, and strict bracket examples.

### `references/04-formatting-rules.md`

Professional formatting instructions for legal, financial, audit, tax, compliance, valuation, Registered Valuer, and CA-practice documents. Defines automatic formatting actions and changes requiring approval.

### `references/05-logical-date-consistency-checks.md`

Checks for dates, timelines, amounts, valuation dates, report dates, financial years, assumptions, identity consistency, visible calculations, and logical contradictions.

### `references/06-ca-legal-financial-sensitivity.md`

Sensitivity rules for legal, tax, audit, compliance, CA-practice, financial, and valuation wording. Includes careful phrasing rules and restrictions on direct rewriting.

### `references/07-section-verification.md`

Canonical section/reference verification and cautious wording rules for statutes, sections, rules, circulars, notifications, standards, IBBI/RV references, valuation rules, and professional standards.

### `references/08-table-numbering-cross-reference.md`

Rules for asking before converting paragraphs into tables, formatting existing tables, checking visible mathematical consistency, reviewing numbering, and checking cross-references.

### `references/09-issue-review-template.md`

Detailed issue-by-issue review template covering structural issues, wording issues, logic/date/amount issues, numbering/cross-reference issues, legal/financial concerns, valuation issues, source verification, and table conversion suggestions.

### `references/10-source-priority-indian-ca-legal-valuation-documents.md`

Indian-specific source priority for CA, legal, tax, compliance, and valuation documents. Extends the general standard in file `12`.

### `references/11-registered-valuer-valuation-report-review.md`

Specialized review guide for Registered Valuer reports, valuation reports, ESOP valuation, Rule 11UA valuation, FEMA/RBI valuation, Companies Act valuation, DCF/NAV/option valuation, assumptions, methodology, dates, calculations, and report completeness.

### `references/12-source-verification-standard.md`

Canonical general source verification standard. Requires authoritative/reputed sources, two-source verification where possible, one-source exception for official sources, current-law verification, verified-only alternative references, and cautious language.

### `references/13-cross-border-valuation-source-map.md`

Cross-border source map for Singapore, United States, UAE, and multi-jurisdiction valuation or corporate documents. Extends file `12` with jurisdiction-specific source priority.

### `references/claude-compatible-prompt.md`

Portable prompt version for Claude or other AI tools. Mirrors the skill workflow, including approval gates, fast path, long-document handling, strict bracket notation, valuation checks, source verification, and change summary requirements.
