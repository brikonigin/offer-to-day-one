---
name: offer-to-day-one-ops
description: Runs the hiring-to-onboarding automation (ATS, project tool, team chat) - tracker syncs, new-hire threads, onboarding projects, late-item nudges and Friday digests.
---

# Offer-to-Day-One ops

The ATS is the record, the project tool is the checklist, team chat is the conversation. This skill keeps the two chat trackers matched to the ATS and the project tool, posts new-hire threads, creates onboarding projects and sends the few messages the SOP allows. It mirrors the SOP's Automation rules (version: `<SOP_VERSION_DATE>`). If the two ever disagree, the SOP wins: stop and tell the recruiting lead.

> **Sanitized example.** Every ID, name and channel below is a placeholder. Replace the values in `<ANGLE_BRACKETS>` with your own.

## Switches (the recruiting lead edits these lines; nothing else changes them)

- NUDGES: shadow   (off | shadow | live). Shadow writes the DMs it would send into the run results only, so owners can confirm the flags are accurate before going live.
- OFFERS_IN_ATS: yes   (no while offers still live outside the ATS; then never nudge or flag offer steps)
- AUTO_PROJECT: on   (creates the onboarding project when an offer is signed)
- OFFER_FORM_SHEET: `<SHEET_ID>`   (responses sheet for the Offer Request and Executive Hire forms)
- WELCOME_EMAIL_DRAFT: on   (draft only, never sent)
- HRIS: off   (on once the HR system connector is available; read-only status checks)

## Which steps to run

| When | Do | Read |
|---|---|---|
| Every scheduled weekday | Onboarding sync | references/onboarding-sync.md |
| Wednesday, after the sync | Hiring Tracker refresh | references/hiring-sync.md |
| Friday, after the sync | Health board, onboarding digest, hiring roll-up. No DMs. | references/friday.md |
| "dry run" or "test" | Every step for today, but write and send nothing. Report what would change. | as above |
| "check against the SOP" | Report every difference between the SOP and references/fields.md. Change nothing. | references/fields.md |

Edge cases (declines, start-date changes, executive hires, contractors, rehires, background check issues) are in references/edge-cases.md; read it only when a row hits one.

## IDs

#onboarding `<CHANNEL_ID>` · Onboarding Tracker `<LIST_ID>` · Health board `<CANVAS_ID>`
#hiring `<CHANNEL_ID>` · Hiring Tracker `<LIST_ID>`
Onboarding project template `<TEMPLATE_ID>`
Recruiting lead `<USER_ID>` · People Ops `<USER_ID>` · People Ops backup `<USER_ID>`. Look anyone else up by company email, once per run.

## Hard rules (from the SOP; never relax them)

1. **Privacy.** #hiring: no candidate names, feedback or pay, ever. #onboarding: names are fine; never pay, ID numbers, bank details, addresses, contact details or background-check results. Project tool: never pay, ID numbers or bank details. Applies to every post, DM, cell, board and project field.
2. **Never overwrite a value a person typed.** Fill blank cells and (auto) columns only. Use only existing options. Never rename columns or options.
3. **Never** move an ATS stage, change a start date anywhere, contact a candidate or new hire, or read pay, ID numbers, bank details, addresses or background-check results.
4. **Messages go only to the person who must act.** Nobody is copied for awareness. At most one DM per person per day, and never more than 3 automated messages per person per day in total, counting digest tags. Never @channel, @here or @everyone.
5. **Before any reminder, re-check the live task.** Never remind anyone about something already done.
6. **Any connector failure or unreadable data:** write nothing, post nothing, send no DMs. DM the recruiting lead once: "🤖 Hiring ops failed: <connector> · <error>".

## Out-of-process safeguards

People will sometimes act outside the SOP. Catch it quietly, route it to the recruiting lead, and let the next run catch up once the record is fixed.

1. **No duplicate projects.** Before creating a project, search for one with the hire's name. One match: link it instead and note "linked existing project (made by hand)". More than one: create nothing and flag it.
2. **Daily cross-check (read only).** Look back 30 days for: an Offer Request with no matching ATS offer; an Executive Hire with no ATS record; an onboarding project with no tracker row; (HRIS on) anyone in the HR system starting in 60 days with no ATS record. From the form sheet read only name, role, team, hiring manager and dates. Never read pay, bonus, equity, relocation or contact columns.
3. **Routing.** Flags go to the recruiting lead only, in one DM, Monday to Thursday, starting "🤖 Out of process:". Repeat a flag only if still open after 5 business days. Never name the person who went around the process in a channel; the digest names only the missing record.
4. Once the ATS is backfilled, treat the hire like any other on the next run.

## Keep it lean (it runs every weekday)

- Read each source once per run. Ask for the fewest fields.
- Skip closed tracker rows entirely.
- One filtered ATS query per run, not one call per candidate.
- Compare before writing; update only changed cells, in batches. A run where nothing changed writes nothing.
- Run results: at most 6 lines. No narration.
