---
name: legal-financial-valuation-document-reviewer-assistant
description: Use when reviewing, formatting, verifying, redlining, or preparing legal, financial, tax, audit, compliance, Chartered Accountant, Registered Valuer, valuation, ESOP, Rule 11UA, Companies Act, IBBI, FEMA, or cross-border valuation documents.
---

# Legal Financial Valuation Document Reviewer Assistant

Use this skill to review and format professional legal, financial, audit, tax, compliance, Chartered Accountant, Registered Valuer, valuation, ESOP, Rule 11UA, Companies Act, IBBI, FEMA, and cross-border valuation documents while preserving meaning, figures, dates, names, legal intent, financial substance, valuation assumptions, regulatory references, and professional presentation.

## Core Operating Rule - Required Gates

Never apply actual text changes without explicit user approval. Formatting-only changes may be done automatically.

Use `references/02-approval-and-gating.md` as the canonical approval rule. Ask only for gates the user has not already clearly answered:

1. Approval before applying text changes.
2. Output format before final output.
3. Clean version, change-marked version, or both.
4. Approval before converting any paragraph into a table.

## Progressive Loading Map

Load only the reference files needed for the current task.

- Full review sequence: `references/01-review-workflow.md`.
- Approval gates and multi-turn approval state: `references/02-approval-and-gating.md`.
- Output format, DOCX fallback, and bracket notation: `references/03-output-formats-and-change-marking.md`.
- Formatting-only work: `references/04-formatting-rules.md`.
- Logical, date, amount, timeline, and visible consistency checks: `references/05-logical-date-consistency-checks.md`.
- Legal, financial, tax, audit, compliance, and CA-practice sensitivity: `references/06-ca-legal-financial-sensitivity.md`.
- Section, rule, law, circular, notification, standard, or valuation reference verification: `references/07-section-verification.md` plus `references/12-source-verification-standard.md`.
- Table conversion, numbering, clauses, annexures, schedules, and cross-references: `references/08-table-numbering-cross-reference.md`.
- Issue-by-issue review format: `references/09-issue-review-template.md`.
- Indian CA, tax, audit, company law, IBBI, Registered Valuer, ESOP, Rule 11UA, FEMA, Companies Act, valuation, or compliance source priority: `references/10-source-priority-indian-ca-legal-valuation-documents.md`.
- Valuation report, ESOP valuation, share valuation, business valuation, Registered Valuer report, merchant banker valuation, DCF, NAV, Rule 11UA, FEMA valuation, Companies Act valuation, or IBBI/RV-related review: `references/11-registered-valuer-valuation-report-review.md`.
- General source verification standard: `references/12-source-verification-standard.md`.
- Singapore, US, UAE, foreign holding companies, foreign subsidiaries, overseas shareholders, cross-border investment, FEMA, ODI, FDI, ESOP to foreign employees, or international valuation context: `references/13-cross-border-valuation-source-map.md`.
- Portable prompt for Claude or another AI tool: `references/claude-compatible-prompt.md`.

**Do not load a reference file unless its trigger condition is clearly met. When in doubt, proceed without it and load only if a specific need arises.**

## Fast Path

If the user explicitly asks for formatting only, with no review, no suggestions, and no text changes:

1. Load `references/04-formatting-rules.md` only.
2. Apply formatting changes automatically.
3. Ask only for output format using `references/03-output-formats-and-change-marking.md`, unless the user already specified it.
4. Do not generate an issue review.
5. Do not ask for approval on text changes because no text changes are being made.
6. Provide a change summary of formatting changes only.

## Long Document Handling

If the document is very long, estimated over 2,000-3,000 words or containing multiple major sections:

1. Confirm whether the user wants all sections reviewed or only specific sections.
2. If reviewing all sections, process section by section and present issues per section before moving to the next.
3. Do not load all reference files upfront for long documents. Load only what is triggered by the section currently being reviewed.
4. Carry forward the approved, rejected, and pending change list across sections.

## Dependencies

- Web search is required for source verification. If unavailable, flag references for manual verification instead of pretending to verify them.
- The `docx` skill is required for actual `.docx` output. If unavailable, offer Word-ready text or Markdown instead.
- Compatibility and packaging notes live in `MANIFEST.md`.

## Default Workflow

For the full step-by-step review sequence, load `references/01-review-workflow.md`.

## Practical Strictness Rule

See `references/05-logical-date-consistency-checks.md`.

## Source Verification Rule

See `references/12-source-verification-standard.md`.

## Final Output Safety

Do not include legal, tax, finance, valuation, professional-review, or source-verification warnings inside the final document unless the user explicitly asks to insert them.

Mention such concerns in the review stage or change summary only.
