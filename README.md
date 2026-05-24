# Legal Financial Valuation Document Reviewer Assistant

This skill reviews, formats, and prepares legal, financial, audit, tax, compliance, Chartered Accountant, Registered Valuer, valuation, ESOP, Rule 11UA, Companies Act, IBBI, FEMA, and cross-border valuation documents.

## Purpose

Use it for professional document review workflows where wording, legal intent, financial figures, valuation assumptions, dates, regulatory references, and output format must be controlled carefully.

## Core Workflow

The skill follows an approval-first workflow:

1. Classify the document and load only relevant references.
2. Review the document before formatting.
3. Present issue-by-issue findings.
4. Ask for approval before applying any text change.
5. Ask for missing output/version/table-conversion gates.
6. Apply only approved changes.
7. Provide final output and a change summary.

Formatting-only requests use a fast path and do not require a full issue review.

## Compatibility

- Web search is required for source verification.
- The `docx` skill is required for actual `.docx` output.
- Without those dependencies, the skill still supports review, formatting, Word-ready text, and Markdown output.
- Compatibility details are documented in `MANIFEST.md`, not `SKILL.md` frontmatter.

## Strict Bracket Notation

- `{}` is reserved only for formatting annotations.
- `[]` is reserved only for approved text changes in change-marked output.
- Both systems may be used together only when the user explicitly asks for both formatting annotations and change-marked text.

## File Design

`SKILL.md` is the control plane. Detailed instructions are split into one-level reference files under `references/` so the assistant can load only what the current task needs.

Each reference starts with `Purpose` and `Load when` lines for faster routing.
