# File Manifest

This manifest explains every file included in the Skill package.

## Root Files

### `SKILL.md`
Primary Skill entrypoint. Contains YAML frontmatter, the trigger description, core approval-first operating rules, progressive loading map, default workflow, practical strictness rule, source verification rule, and final output safety rule.

### `README.md`
User-facing documentation explaining the Skill purpose, workflow, key capabilities, file design, and production rules.

### `MANIFEST.md`
This file. Lists each bundled file with its purpose and key contents.

## Configuration

### `agents/openai.yaml`
ChatGPT UI metadata. Defines display name, short description, icon, and primary color.

## Reference Files

### `references/01-review-workflow.md`
End-to-end review workflow for intake, document classification, issue review, approval gates, table conversion gate, output format gate, final formatting, and change summary.

### `references/02-approval-and-gating.md`
Approval rules defining what counts as a text change, required approval gates, approval options, ambiguous approval handling, and sensitive issue handling.

### `references/03-output-formats-and-change-marking.md`
Output format rules for Word-ready text, Markdown, detailed formatting annotations using `{}`, change-marked Markdown using `[]`, DOCX comments/tracked-change handling, and final document restrictions.

### `references/04-formatting-rules.md`
Professional formatting instructions for legal, financial, audit, tax, compliance, valuation, Registered Valuer, and CA-practice documents. Defines automatic formatting actions and changes requiring approval.

### `references/05-logical-date-consistency-checks.md`
Detailed checks for dates, timelines, amounts, valuation dates, report dates, financial years, assumptions, identity consistency, and visible logical contradictions.

### `references/06-ca-legal-financial-sensitivity.md`
Sensitivity rules for legal, tax, audit, compliance, CA-practice, financial, and valuation wording. Includes careful phrasing rules and restrictions on direct rewriting.

### `references/07-section-verification.md`
Rules for verifying statutes, sections, rules, circulars, notifications, standards, IBBI/RV references, valuation rules, and professional standards against authoritative sources.

### `references/08-table-numbering-cross-reference.md`
Rules for asking before converting paragraphs into tables, formatting existing tables, checking visible mathematical consistency, reviewing numbering, and checking cross-references.

### `references/09-issue-review-template.md`
Detailed issue-by-issue review template covering structural issues, wording issues, logic/date/amount issues, numbering/cross-reference issues, legal/financial concerns, valuation issues, source verification, and table conversion suggestions.

### `references/10-source-priority-indian-ca-legal-valuation-documents.md`
Source hierarchy for Indian CA, legal, tax, compliance, and valuation documents. Covers IBBI, MCA, Income Tax, ICAI, CBIC/GST, RBI, SEBI, case law, and reputed secondary sources.

### `references/11-registered-valuer-valuation-report-review.md`
Specialized review guide for Registered Valuer reports, valuation reports, ESOP valuation, Rule 11UA valuation, FEMA/RBI valuation, Companies Act valuation, DCF/NAV/option valuation, assumptions, methodology, dates, calculations, and report completeness.

### `references/12-source-verification-standard.md`
General source verification standard. Requires authoritative/reputed sources, two-source verification where possible, one-source exception for official sources, current-law verification, and verified-only alternative references.

### `references/13-cross-border-valuation-source-map.md`
Cross-border source map for Singapore, United States, UAE, and multi-jurisdiction valuation or corporate documents. Includes source hierarchy and jurisdiction rules.

### `references/claude-compatible-prompt.md`
Portable prompt version for Claude or other AI tools. Mirrors the Skill workflow in prompt form, including approval gates, output format rules, valuation checks, source verification, and change summary requirements.
