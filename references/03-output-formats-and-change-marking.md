# Output Formats and Change Marking

> Purpose: Canonical output format choices, DOCX fallback behavior, and strict bracket notation rules.
> Load when: The user must choose output format, asks for Markdown annotations, asks for change-marked output, or requests DOCX.

> Final output rule: see `SKILL.md` - `Final Output Safety`.

## Contents

- Output format options
- Version type options
- Strict bracket separation
- Formatting annotation rules
- Change-marked Markdown rules
- DOCX output fallback
- Examples

## Output Format Options

Ask only if the user has not already specified the output format:

Which output format would you like?

A. Word-ready format  
B. Markdown format  
C. Markdown with detailed formatting annotations using `{}`  
D. Change-marked Markdown using `[]`  
E. DOCX file  
F. Both clean version and change-marked version  
G. Both Word-ready text and Markdown  

Do not assume the user wants Word output.

Do not offer DOCX if the `docx` skill is unavailable. Substitute Word-ready text and say: "DOCX file output requires the docx skill. I can provide Word-ready text instead."

## Version Type Options

Ask only if the user has not already specified version type:

Which version type do you want?

A. Clean final version only  
B. Change-marked version only  
C. Both clean final version and change-marked version  

## Strict Bracket Separation

Use bracket notation strictly:

- `{}` is reserved only for formatting annotations.
- `[]` is reserved only for approved text changes in change-marked output.
- Do not use `{}` to show text changes.
- Do not use `[]` for formatting instructions.
- Use both systems together only if the user explicitly asks for both formatting annotations and change-marked text.
- Do not invent inline formatting tags.

## Markdown with Detailed Formatting Tags

If the user chooses Markdown with formatting annotations, use curly brackets `{}` only for formatting instructions.

Use detailed tags such as:

- `{Document Title: Bold, Center Aligned, 16 pt, All Caps}`
- `{Heading 1: Bold, Left Aligned, 14 pt, Before Spacing 12 pt, After Spacing 6 pt}`
- `{Heading 2: Bold, Left Aligned, 12 pt, Numbered}`
- `{Body Paragraph: Justified, 11 pt, 1.15 Line Spacing}`
- `{Important Date: Bold}`
- `{Important Amount: Bold}`
- `{Valuation Conclusion: Bold, Boxed, Light Grey Shading}`
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

If a change involves deletion, mention the deletion in the change summary instead of silently hiding it.

## DOCX Output

This output option requires the `docx` skill. If the `docx` skill is not available, do not offer DOCX as an output option. Offer Word-ready text or Markdown instead.

If the user chooses DOCX output:

1. Prefer tracked-changes style if technically supported.
2. If tracked changes are not technically supported, use Word comments.
3. If neither is technically available, provide:
   - Clean DOCX version
   - Separate change summary
   - Optional change-marked text version if the user requested it

For DOCX change-marked output, avoid inserting visible brackets inside the document unless the user specifically asks for visible bracket markings.

## Examples

### Formatting Annotations Only

Input:

```text
Agreement
This agreement is made on 1 January 2024 between ABC Private Limited and XYZ Limited.
```

Output:

```markdown
{Document Title: Bold, Center Aligned, 16 pt, All Caps}
AGREEMENT

{Body Paragraph: Justified, 11 pt, 1.15 Line Spacing}
This agreement is made on 1 January 2024 between ABC Private Limited and XYZ Limited.
```

### Change-Marked Text Only

Input:

```text
The report was issue on 12 March 2024.
```

Output:

```markdown
The report was [issued] on 12 March 2024.
```

### Combined Output Only When Explicitly Requested

```markdown
{Body Paragraph: Justified, 11 pt, 1.15 Line Spacing}
The report was [issued] on 12 March 2024.
```
