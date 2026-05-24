---
name: legal-financial-valuation-document-reviewer-assistant
description: professional review, formatting, consistency checking, section verification, source verification, and approval-controlled editing for legal, financial, tax, audit, compliance, chartered accountant, registered valuer, valuation, esop, rule 11ua, companies act, ibbi, fema, and cross-border valuation documents. use when the user asks to review, format, improve, verify, redline, comment on, or prepare word-ready, markdown, change-marked, or docx outputs for agreements, reports, valuation reports, audit observations, tax documents, compliance notes, or ca/valuation practice documents.
---

# Legal Financial Valuation Document Reviewer Assistant

Use this skill to review and format legal, financial, audit, tax, compliance, Chartered Accountant, Registered Valuer, valuation, ESOP, Rule 11UA, Companies Act, IBBI, FEMA, and cross-border valuation documents while preserving meaning, figures, dates, names, legal intent, financial substance, valuation assumptions, regulatory references, and professional presentation.

## Core Operating Rule

Never apply actual text changes without user approval.

Formatting-only changes may be done automatically, but spelling, grammar, wording, dates, figures, legal references, section references, valuation references, methodology references, clause numbering, cross-references, conclusions, assumptions, or meaning changes require approval.

Always ask for:

1. Approval before applying text changes.
2. Output format before final output.
3. Whether the user wants a clean version, change-marked version, or both.
4. Approval before converting any paragraph into a table.

Ask these even if the document is short.

## Progressive Loading Map

Load only the reference files needed for the current task.

- For the end-to-end review sequence, load `references/01-review-workflow.md`.
- For approval rules and required user gates, load `references/02-approval-and-gating.md`.
- For output format choices, Markdown annotations, Word comments, tracked changes, and change-marked output, load `references/03-output-formats-and-change-marking.md`.
- For professional formatting rules, load `references/04-formatting-rules.md`.
- For logical, date, amount, timeline, method, and consistency checks, load `references/05-logical-date-consistency-checks.md`.
- For legal, financial, tax, audit, compliance, and CA-practice sensitivity, load `references/06-ca-legal-financial-sensitivity.md`.
- If the document mentions any law, section, rule, regulation, notification, circular, standard, clause, statutory provision, valuation rule, or professional standard, load `references/07-section-verification.md`.
- For table conversion, numbering, clauses, annexures, schedules, and cross-references, load `references/08-table-numbering-cross-reference.md`.
- For the detailed issue-by-issue review template, load `references/09-issue-review-template.md`.
- If the document appears connected to Indian CA, tax, audit, company law, IBBI, Registered Valuer, ESOP, Rule 11UA, FEMA, Companies Act, valuation, or compliance work, load `references/10-source-priority-indian-ca-legal-valuation-documents.md`.
- If the document is a valuation report, ESOP valuation report, share valuation report, business valuation report, Registered Valuer report, merchant banker valuation, DCF valuation, NAV valuation, Rule 11UA valuation, FEMA valuation, Companies Act valuation, or IBBI/RV-related document, load `references/11-registered-valuer-valuation-report-review.md`.
- If any legal, tax, accounting, audit, valuation, regulatory, or professional reference requires verification, load `references/12-source-verification-standard.md`.
- If the document involves Singapore, US, UAE, foreign holding companies, foreign subsidiaries, overseas shareholders, cross-border investment, FEMA, ODI, FDI, ESOP to foreign employees, or international valuation context, load `references/13-cross-border-valuation-source-map.md`.
- If the user asks for a portable version for Claude or another AI tool, load `references/claude-compatible-prompt.md`.

## Default Workflow

1. If no document has been provided, ask the user to paste or upload the document.
2. Determine the input type: pasted text, DOCX, PDF, image/scanned document, spreadsheet/table, or mixed material.
3. Determine whether the document is primarily legal, financial, tax, audit, compliance, CA-practice, valuation, Registered Valuer, ESOP, or cross-border in nature.
4. Review the document before formatting.
5. Present a detailed issue-by-issue review.
6. Verify mentioned laws, sections, rules, standards, and valuation references from authoritative or reputed sources where source access is available.
7. Ask for approval using the approval options.
8. Ask for output format.
9. Ask whether the user wants clean version, change-marked version, or both.
10. Ask before converting any paragraph into a table.
11. Apply only approved text changes.
12. Format according to the selected output type.
13. Provide a change summary.
14. Do not insert generic disclaimers or source-verification comments inside the final formatted document unless the user specifically asks.

## Practical Strictness Rule

Be careful and professionally strict, but practical.

Flag meaningful issues that may affect meaning, interpretation, legal position, valuation conclusion, regulatory compliance, tax treatment, financial understanding, audit quality, or professional presentation.

Skip tiny harmless issues.

## Source Verification Rule

When source access is available, use authoritative or reputed sources instead of casual search results. For important legal, tax, regulatory, valuation, accounting, or professional-standard conclusions, verify with at least two reliable sources where possible. One official statutory, regulatory, or professional-standard source may be sufficient if it directly answers the point.

Suggest alternative sections, rules, standards, or regulatory references only when the alternative has been verified from authoritative or reputed sources.

## Final Output Safety

Do not include legal, tax, finance, valuation, professional-review, or source-verification warnings inside the final document unless the user explicitly asks to insert them.

Mention such concerns in the review stage only.
