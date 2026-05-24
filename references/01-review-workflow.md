# Review Workflow

> Purpose: Step-by-step intake, classification, review, approval, and output sequence for professional document review.
> Load when: The user asks for a full review, correction, redline, verification, or final preparation workflow.

## Contents

- Intake and document classification
- Reference file routing by document type
- First review before formatting
- Approval, table, output, and version gates
- Approved-change application and final summary

## Step 1: Intake

Identify the input type:

- Pasted text
- DOCX document
- PDF
- Scanned PDF or image
- Spreadsheet/table
- Mixed documents
- Extracted OCR text
- User-provided draft clauses or report sections

If the document is unclear, incomplete, or appears extracted from OCR, mention that some formatting or text may need confirmation.

Do not ask unnecessary questions if the task can proceed.

## Step 2: Classify the Document

Determine whether the document is primarily:

- Legal agreement or contract
- Financial report
- Audit observation
- Tax or compliance document
- Chartered Accountant practice document
- Registered Valuer or valuation report
- ESOP, Rule 11UA, FEMA/RBI, IBBI, or Companies Act valuation document
- Cross-border valuation or corporate document
- Mixed or unclear

Use this classification to load only the relevant reference files.

### Files to Load Based on Document Type

| Document type | Load these files |
|---|---|
| Any full review | `04`, `05`, `06`, `08`, `09` |
| Has legal, statutory, regulatory, standard, or valuation references | `07`, `12` |
| Indian CA, IBBI, ESOP, Rule 11UA, Companies Act, FEMA, tax, audit, or valuation source priority | `10` |
| Valuation report, RV report, ESOP valuation, DCF, NAV, Rule 11UA, FEMA valuation, Companies Act valuation | `11` |
| Cross-border, Singapore, US, UAE, foreign shareholder, ODI, FDI, or international valuation context | `13` |
| User asks for actual DOCX output | `docx` skill |

Do not load every file by default. Load a file only when the document type or current section clearly triggers it.

## Step 3: First Review Before Formatting

Before formatting, perform a detailed review under these categories:

1. Structural and formatting issues
2. Spelling, grammar, and wording suggestions
3. Logical, consistency, and date issues
4. Numbering and cross-reference issues
5. Legal, financial, tax, audit, compliance, or CA-practice concerns
6. Valuation, Registered Valuer, ESOP, and methodology issues, if applicable
7. Section, rule, law, circular, notification, standard, or valuation reference verification issues, if applicable
8. Table conversion suggestions

Use `09-issue-review-template.md` for the review format.

## Step 4: Approval Gate

Before applying any text change, ask the user to approve, reject, or selectively approve suggested changes.

Use `02-approval-and-gating.md`.

## Step 5: Table Conversion Gate

If any paragraph may be clearer as a table, ask before converting it.

This applies to every paragraph, not only financial data.

Use `08-table-numbering-cross-reference.md`.

## Step 6: Output Format Gate

Ask for output format only if the user has not already specified it.

Use `03-output-formats-and-change-marking.md`.

## Step 7: Clean or Change-Marked Gate

Ask whether the user wants a clean version, change-marked version, or both only if the user has not already specified it.

Use `03-output-formats-and-change-marking.md`.

## Step 8: Apply Approved Changes Only

Apply only the changes approved by the user.

If approval is ambiguous, apply only the clearly approved changes and mention what was not applied.

Use the multi-turn state rule in `02-approval-and-gating.md`.

## Step 9: Format the Document

Use professional formatting suitable for legal, financial, audit, tax, compliance, valuation, Registered Valuer, or Chartered Accountant practice documents.

Use `04-formatting-rules.md`.

## Step 10: Final Change Summary

After the final output, include a change summary with:

1. Approved text changes applied
2. Approved date or consistency corrections applied
3. Approved numbering or cross-reference corrections applied
4. Approved valuation, source, or regulatory reference corrections applied
5. Formatting changes made automatically
6. Issues flagged but not changed

If no text changes were applied, state:

"No text changes were applied. Only formatting changes were made."
