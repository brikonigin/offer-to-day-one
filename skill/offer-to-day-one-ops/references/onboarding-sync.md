# Onboarding sync (every scheduled weekday)

## 1. Gather (read only, once each)

- **Tracker:** every row. Set aside rows whose Attention (auto) is Closed.
- **ATS:** one query for applications at offer stage or later (needs offer, awaiting approval, awaiting acceptance, accepted, declined, hired), updated in the last 30 days (90 on Fridays, for the health board), plus every application linked on an open tracker row. Keep: application ID, name, job, stage, stage entered date, offer status, start date, hiring manager email, employment type, location, source.
- **Match rows to the ATS by application ID, never by name.**
- **Project tool:** for each open row, read the linked project's tasks (name, assignee, due date, completed).

## 2. Update the tracker (silent, changed cells only)

- New row for any application at offer stage or later with no row: name, role, start date, employment type, ATS link, Status = Offer in progress. Hiring manager: the chat user matching the ATS hiring manager's email; if none, add "Missing: Hiring manager".
- Decline in the ATS: Status = Offer declined, Attention = Closed.
- Project tasks → checklist columns, per references/fields.md. If a filled cell disagrees with the project, leave it and add "Check: project shows <task> <done/not done>; tracker says <value>".

## 3. New-hire thread

For each hire with an accepted offer and no thread, post once in #onboarding:

```
New hire: <name>
Role:
Team:
Hiring manager: <@hiring manager>
Start date:
Location / remote:
Day-1 buddy:
ATS: <link>
```

Reply in the thread: "<@People Ops> Offer signed. The onboarding project is ready: <link>. Please check the start date and owners." Never post a second thread for a hire.

## 4. Onboarding project

- Create from the template, named `Onboarding: First Last (M/D)`, with owners set and due dates counted in business days from the start date (see templates/onboarding-checklist.md). Run the duplicate check first.
- Assign unassigned tasks to the row's hiring manager.
- From the Offer Request response, copy only: role, team, hiring manager, reports to, employment type, location, start date, Day-1 buddy, computer type, apps and access, special needs. Put computer type on the laptop task and apps on the access task. **Never copy pay, bonus, equity, relocation or any amount.**

## 5. Attention and sync notes

- Attention: Late if any open task is past due; else Due soon if due within 1 business day; else Missing info; else On track.
- Hire not in the ATS and nothing vouches for it: "Check: confirm this hire is real". A project or thread exists but no ATS record: "Check: not in ATS (executive hire?)".

## 6. Nudges (Monday to Thursday only)

The project tool already reminds people about tasks that are due. This step covers only work that is **late**.

1. Candidates: open tasks at least 1 business day past due.
2. Re-fetch each task. Drop it if now complete, if the tracker already shows it done, or if a blocker is set for that item.
3. Drop anything nudged the previous business day.
4. One DM per owner: "🤖 Onboarding sync:" then one line per item (hire · task · was due <date>). If the owner is out, route to their named backup. Keep the 3-per-day cap.
5. NUDGES live: send. Shadow: list would-be DMs in run results only. Off: skip.

## 7. Welcome email draft

On the business day before the welcome-email task is due, read the hiring manager's Day-1 details in the thread and draft the welcome email to the new hire, cc the hiring manager, for the recruiting lead to review and send. **Never send it.** If the Day-1 details are missing, skip; the Day-1 task will show as late.
