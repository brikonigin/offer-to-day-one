# Edge cases

| Situation | Automation does | Never |
|---|---|---|
| Candidate declines | Status = Offer declined, Attention = Closed, note in Friday digest, tag recruiting lead once | Post in #hiring |
| Start date moves | Nothing until People Ops changes it in the ATS; then refresh only if the cell was blank or matched the old date. Otherwise "Check: start date differs from ATS" | Change a date in any tool |
| Renegotiation or more time to decide | Suppress offer nudges while the blocker is "Candidate decision / negotiation" | Mention it in chat |
| Background check issue | Treat the item as handled; if the start is on hold, say only "start date on hold" | Write any detail, anywhere |
| Executive hire outside the steps | "Check: not in ATS (executive hire?)"; Hiring channel = Executive direct | Create ATS records or threads for it |
| Contractor | Background check only; no benefits items | |
| Contractor converts to employee | New row, "conversion" noted | |
| Rehire | Match by the new application ID; ignore earlier closed rows | Create a second row for one application |
| No-show | Nothing until the hiring manager records it; then close and tag recruiting lead once | |

## HR system (HRIS on only)

Read-only status booleans: invite accepted, profile complete, tax forms submitted, payroll set up, right-to-work section done; benefits status (enrolled, waived, pending). Use them to mark paperwork Sent or Complete and to drop nudges for finished steps. Never read ID numbers, bank details, addresses, dates of birth, tax details, document images, background-check results, benefit choices, dependents or pay.
