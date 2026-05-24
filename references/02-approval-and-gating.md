# Approval and Gating Rules

> Purpose: Canonical approval gates, approval menu, and multi-turn approval tracking.
> Load when: Any text change, table conversion, approval response, or final-output gate is involved.

> Final output rule: see `SKILL.md` - `Final Output Safety`.

## Contents

- Non-negotiable approval rule
- Required gates
- Approval options
- Handling user approval
- Multi-turn state rule

## Non-Negotiable Approval Rule

Formatting changes do not require approval.

Actual text changes require approval.

Treat the following as actual text changes:

- Spelling correction
- Grammar correction
- Rephrasing
- Sentence restructuring
- Adding words
- Removing words
- Reordering text
- Changing legal wording
- Changing financial wording
- Changing valuation wording
- Changing assumptions
- Changing methods or methodology descriptions
- Changing numbers
- Changing amounts
- Changing percentages
- Changing dates
- Changing names
- Changing party details
- Changing clause references
- Changing statutory sections
- Changing valuation rules or standards
- Changing conclusions
- Changing observations
- Changing recommendations
- Correcting numbering
- Correcting cross-references

If unsure whether a change is formatting or text, treat it as a text change.

## Required Gates

Ask for these before final output unless the user already clearly answered them:

1. Approval for text changes
2. Approval before converting any paragraph into a table
3. Preferred output format
4. Clean version, change-marked version, or both

Ask even for short documents when the gate is relevant and unanswered.

## Approval Options

After the issue review, ask the user:

Please choose how you want me to proceed:

A. Approve all suggested text changes and corrections  
B. Approve only selected changes  
C. Reject all text changes and format original text only  
D. Fix only spelling and grammar, but do not rephrase legal, financial, or valuation wording  
E. Apply formatting only and keep all wording exactly unchanged  
F. Show both a clean version and a change-marked version  
G. Ask me questions before making any final changes  

## Handling User Approval

If the user approves all:
- Apply all suggested text changes.

If the user approves selected items:
- Apply only selected items.

If the user rejects all:
- Keep wording exactly unchanged.
- Apply formatting only.

If the user says "do whatever is best":
- Do not treat that as approval for legal, financial, valuation, date, number, section, methodology, assumption, or meaning changes.
- Ask for explicit approval where required.

If the user asks for direct final output without approval:
- Provide formatting-only output unless the user clearly approved text changes.

## Multi-Turn State Rule

Maintain a running internal list of approved, rejected, and pending items across the conversation.

After each user approval response, confirm what was approved and what was not before proceeding.

Use this confirmation format:

- Approved: [issue numbers]
- Rejected: [issue numbers]
- Pending: [issue numbers not yet addressed]

Apply only the approved items in the final output step.
