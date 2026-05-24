# Legal Financial Valuation Document Reviewer Assistant

This Skill reviews, formats, and prepares legal, financial, audit, tax, compliance, Chartered Accountant, Registered Valuer, valuation, ESOP, Rule 11UA, Companies Act, IBBI, FEMA, and cross-border valuation documents.

## Purpose

The Skill is designed for professional document review workflows where wording, legal intent, financial figures, valuation assumptions, dates, regulatory references, and output format must be controlled carefully.

It follows an approval-first workflow:

1. Review the document.
2. Present a detailed issue-by-issue review.
3. Ask for approval before applying any wording/text change.
4. Ask for output format every time.
5. Ask whether the user wants a clean version, change-marked version, or both.
6. Ask before converting paragraphs into tables.
7. Apply only approved text changes.
8. Provide the final document and change summary.

## Key Capabilities

- Legal and financial report formatting
- Spell-checking and wording suggestions
- Logical, consistency, amount, date, and timeline review
- Numbering and cross-reference review
- CA, tax, audit, compliance, and company law sensitivity checks
- Registered Valuer and valuation report review
- ESOP, Rule 11UA, FEMA/RBI, Companies Act, IBBI, and cross-border valuation review
- Source verification from authoritative or reputed sources
- Word-ready, Markdown, annotated Markdown, change-marked Markdown, and DOCX-oriented output workflows
- Claude-compatible portable prompt included in `references/claude-compatible-prompt.md`

## File Design

`SKILL.md` is intentionally compact and acts as the control plane. Detailed instructions are split into one-level reference files under `references/` so the assistant loads only the instruction set needed for the current task.

## Important Production Rules

- Do not apply actual text changes without approval.
- Do not add generic disclaimers inside final documents.
- Keep legal, tax, financial, valuation, and source-verification comments in the review stage unless the user asks to include them in the final document.
- Verify important references using authoritative or reputed sources where possible.
- Suggest alternative statutory or regulatory references only when verified.
