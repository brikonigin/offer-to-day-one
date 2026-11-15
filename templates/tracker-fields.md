# Tracker fields

Keep option lists short and fixed. The automation only uses options that exist.

## Onboarding Tracker (one row per new hire)

| Field | Options | Set by | Automation may |
|---|---|---|---|
| Status | Offer in progress · Offer accepted · Pre-start in progress · Ready for Day 1 · Started · Week 1 complete · Offer declined · Rescinded / no-show | People Ops | Fill blank; set Offer declined from the ATS (the only overwrite) |
| Background check | Not started · In progress · Cleared · Issue · Not required | People Ops | Fill blank with In progress. Never Cleared or Issue |
| Paperwork / payroll | Not started · Sent · Complete | People Ops | Fill blank from the project tool |
| Equipment / IT | Not started · Ordered · Shipped / ready · Not needed | IT | Fill blank from the project tool |
| Accounts | Not started · Requested · Created | IT | Fill blank from the project tool |
| Site access | Not needed · Requested · Ready | Hiring manager | Fill blank with Not needed for remote roles |
| Blocker type | Offer approval · Candidate decision / negotiation · Background check · Paperwork / payroll · Equipment / IT · Accounts / access · Site access · Manager availability · Other | Whoever is blocked | Never |
| Day-1 outcome | On time, fully ready · On time, items missing · Start date moved · No-show / rescinded | Hiring manager | Never |
| Hiring channel | Job board · Referral · Executive direct | People Ops | Fill blank from the ATS source |
| Employment type | Full-time · Part-time · Contractor | People Ops | Fill blank from the ATS |
| Attention (auto) | Late · Due soon · Missing info · On track · Closed | Sync | Always |
| Sync notes (auto) | Allowed lines only (below) | Sync | Always |

**Allowed sync-note lines:** `Late: <item> was due <date>` · `Missing: <field>` · `Check: <discrepancy>` · `Not updated since <date>` · `Blocked since <date>` · `Nudged <date>: <item>` · `Project: <url>` (always last)

## Hiring Tracker (one row per open role, never per candidate)

| Field | Options | Set by |
|---|---|---|
| Status | Not yet open · JD in progress · Sourcing · Screening · Interviewing · Offer out · Filled · On hold | Hiring manager |
| Health | Stalled · Needs attention · On track · Not open yet · On hold · Filled | Recruiting lead |
| Next step, Blocker | Free text, role-level only | Hiring manager |
| Pipeline snapshot (auto) | Counts by stage, no names | Sync |
