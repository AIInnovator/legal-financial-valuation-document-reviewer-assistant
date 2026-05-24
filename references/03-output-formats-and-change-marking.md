# Output Formats and Change Marking

## Always Ask Output Format

Before final output, ask:

Which output format would you like?

A. Word-ready format  
B. Markdown format  
C. Markdown with detailed formatting annotations using `{}`  
D. Change-marked Markdown using `[]`  
E. DOCX file  
F. Both clean version and change-marked version  
G. Both Word-ready text and Markdown  

Do not assume the user wants Word output.

## Always Ask Version Type

Ask:

Which version type do you want?

A. Clean final version only  
B. Change-marked version only  
C. Both clean final version and change-marked version  

## Markdown with Detailed Formatting Tags

If the user chooses Markdown with formatting annotations, use curly brackets `{}` only for formatting instructions.

Use detailed tags.

Examples:

- `{Document Title: Bold, Center Aligned, 16 pt, All Caps}`
- `{Heading 1: Bold, Left Aligned, 14 pt, Before Spacing 12 pt, After Spacing 6 pt}`
- `{Heading 2: Bold, Left Aligned, 12 pt, Numbered}`
- `{Body Paragraph: Justified, 11 pt, 1.15 Line Spacing}`
- `{Defined Term: Bold}`
- `{Important Date: Bold}`
- `{Important Amount: Bold}`
- `{Valuation Conclusion: Bold, Boxed, Light Grey Shading}`
- `{Legal Warning: Bold, Text Color Red}`
- `{Note: Italic, Light Grey Shading}`
- `{Table: Clean Borders, Header Row Bold, Header Row Shaded, Amounts Right Aligned}`
- `{Clause: Numbered, Hanging Indent}`
- `{Sub-Clause: Lowercase Alphabetical Numbering, Indented}`
- `{Page Break}`
- `{Signature Block: Left Aligned, Spacing Before 18 pt}`

Do not use `{}` to show text changes.

## Change-Marked Markdown

If the user chooses change-marked Markdown, use square brackets `[]` only for approved text that was newly added, corrected, or incorporated.

Example:

Before:
The report was issue on 12 March 2024.

After:
The report was [issued] on 12 March 2024.

Do not use `[]` for formatting instructions.

If a change involves deletion, mention the deletion in the change summary instead of silently hiding it.

## DOCX Output

If the user chooses DOCX output:

1. Prefer tracked-changes style if technically supported.
2. If tracked changes are not technically supported, use Word comments.
3. If neither is technically available, provide:
   - Clean DOCX version
   - Separate change summary
   - Optional change-marked text version if the user requested it

For DOCX change-marked output, avoid inserting awkward visible brackets inside the document unless the user specifically asks for visible bracket markings.

## Final Document Rule

Do not insert generic legal, tax, finance, valuation, source-verification, or professional-review warnings inside the final formatted document unless the user explicitly asks.

Concerns may be mentioned in the review stage, not embedded into the final document.
