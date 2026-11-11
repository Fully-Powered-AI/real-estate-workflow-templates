# Property owner report

Capability template, version 0.1.0.

## Purpose

Draft the month's report from a property manager to a building's owner, from the statements and logs the manager supplies: occupancy, collections, open maintenance and the decisions the owner is asked to make. Every statement carries a tag naming its source, every figure is recomputed from the supplied rows, and whatever the records cannot support is listed as a gap instead of being written as fact. The assistant prepares; it values nothing, advises on no leasing, purchase or sale decision, changes no record and sends nothing. The property manager and the accountant verify the draft before the owner sees it.

## When to use it and when not to

Use it once the month's statements and logs are in, before the report goes to the owner. Run it again when a late statement arrives or a correction is made.

Do not use it:

- to value the property, set or review rents, or say whether to renew, lease, sell or buy. Those belong to the owner and the people the owner relies on;
- to explain why expenses moved or to produce a budget variance analysis. This report quotes the statement's rental income line and nothing else from the statement;
- to check the rent roll against the lease record. That is a separate piece of work to do first if the roll is in doubt;
- as a weekly business brief for an owner-operator, or a status update on a project;
- when the operating statement is for a different month than the one reported. Stop and ask.

## Roles

- **Runs it:** the property manager, or an assistant working for the manager.
- **Verifies collections and statement figures:** the accountant who prepared the statements.
- **Verifies occupancy, maintenance, notes and gaps, and approves the draft:** the property manager.
- **Decides each item listed under decisions requested:** the owner.
- **Sends the report:** a person. The assistant never does.

## Inputs

The assistant works from files and notes the person supplies. It needs no connection to a property system and never asks for a password or a login code. Default column headers are given for each export. If a header does not match, do not guess: stop, show the headers that were found and ask which column is which.

1. **Settings.** Property name, month, period end, today's date. Optional: staleness limit (default 5 days), long-open limit (default 30 days), lease window (default 90 days). If the property name, month or period end is missing, stop and ask.
2. **Operating statement** for the month. Default headers: Account, Current Month, Prior Month, Budget. The report uses the line for rental income collected (called "Rental Income" or similar; if more than one line could be it, ask). If the statement is missing, write "operating statement not supplied" in the collections section and continue.
3. **Leasing tracker** as of the period end. Default headers: Unit, Tenant, Status, Area (sq ft), Monthly Rent, Lease End, Move-In Date, Move-Out Date. Status values are Occupied, Notice or Vacant. If the tracker is missing, stop: occupancy cannot be reported. A blank Area for any unit means no area-based rate is given. Monthly Rent is not used in the report, and a charged amount that differs from it is neither compared nor mentioned.
4. **Collections report** for the month. Default headers: Unit, Tenant, Charged, Received, Balance, Days Past Due. Balance is the total owed at the period end, including earlier months. If missing, write "collections report not supplied" and continue.
5. **Work-order summary** with its as-of date. Default headers: Work Order, Unit or Area, Description, Date Opened, Status, Date Closed, Last Updated. Status values are Open, In Progress, Waiting or Closed. If missing, write "work-order summary not supplied" and continue.
6. **Manager notes,** numbered N1, N2 and so on. A note that asks the owner for a decision starts with "Decision for owner". If the person supplies unnumbered notes, number them in the order given and say so. A note is linked to a work order only if it names the work order's number.
7. **Last month's report,** for its occupancy figure and its decisions. If missing, say in the gaps that carried decisions and the prior comparison were not checked.

## The procedure

1. **Check the inputs.** Confirm one property and one month across the files. A name or month that disagrees is a stop. A unit that appears twice in the tracker or the collections report is a stop: ask which row is right. A Status value outside the lists above is a stop: ask what it means.
2. **Tag every statement.** Source tags: [S] operating statement, [L] leasing tracker, [C] collections report, [W] work-order summary, [P] last month's report, [N1], [N2] and so on for manager notes. A statement may carry more than one tag. A statement with no tag is not written.
3. **Occupancy.** Count units by Status. Occupied units are Occupied plus Notice; show the two counts separately. Rate by units = occupied units divided by all units, to one decimal. Rate by area = occupied area divided by all area, to one decimal, only if every unit has an Area. Compare with last month's rate from [P]; if [P] is missing, write "not compared". List move-ins and move-outs whose date falls in the month, and units on notice with their move-out date. List every lease ending within the lease window after the period end, soonest first, including a unit on notice. List separately any occupied unit whose Lease End is before the period end, with what the tracker and any note say about a renewal. A tenant change that appears only in a note, or a tracker status a note contradicts, is unconfirmed and goes to the gaps.
4. **Collections.** Total Charged and Received from the rows. Collection rate = Received divided by Charged, to one decimal. Unpaid charges for the month = Charged minus Received, in total. If a row's Balance is less than its own Charged minus Received, show it as supplied and add a gap. List every unit with a Balance above zero, largest Days Past Due first, with the balance, the days, and the part of the balance that is earlier months (Balance minus that month's unpaid charge). Quote the statement's rental income line for the month, the prior month and the budget, with the differences. Compare the statement's rental income with the collections report's Received total; if they differ, state both figures and the difference as a question for the accountant, and use [C] for rates. Record any payment arrangement only as the manager's note states it.
5. **Open maintenance.** Compare the as-of date of [W] with the period end. If it is earlier by more than the staleness limit, say so at the top of the section and in the gaps: later changes are not shown. Count work orders not closed, by status. Age = days from Date Opened to the period end. List first those open longer than the long-open limit, oldest first, then the rest, also oldest first; each line has the work order, place, description, date opened, age, status and last updated. Count work orders closed in the month by Date Closed and list their numbers. Any work order a note names that is not in [W] goes to the gaps.
6. **Explanations.** A manager's explanation of a result, such as why collections fell, is written as "Manager's explanation [N]" and followed by what the records show about the facts it names. State plainly what the records do not show, such as how much each cause accounts for. A forecast or an assertion about a past period that no supplied record supports is not written into the body, however harmless (a count of showings, for example); list it in the gaps with the note number.
7. **Decisions requested.** List each "Decision for owner" note as a question with the facts from the records, any amount and any deadline exactly as the note gives them. List new decisions in note order. Then carry forward every decision listed in [P] that no note records as settled, marked "carried forward". List any decision [P] carried that a note records as settled under "Settled since the last report". Recommend nothing. If a decision is about leasing terms, a purchase, a sale or a valuation, list it as the manager worded it and add no view.
8. **Gaps and unconfirmed items.** Collect, with source tags: inputs not supplied or stale; figures that differ between two documents; unconfirmed tenant changes; notes the records do not support; anything stopped on in a single row. Write "None." if empty.
9. **Summary.** Write it last from the sections, one line each for occupancy, collections, open maintenance, decisions and gaps, with the counts matching the sections below.
10. **Return the draft** to the property manager, with the verification line for the manager and the accountant. A person sends the report after both have verified it.

## Exceptions and stop conditions

- **Files disagree on property or month, a unit appears twice, a status is not recognised, or a header does not match:** stop and ask.
- **The leasing tracker is missing:** stop.
- **A note names an eviction, a legal notice or a dispute:** report only what the note says and the amount from the records, with no view on legal steps; the owner takes those to their own advisers.
- **A note describes a tenant's health, family or other personal circumstances:** leave it out and refer to the unit and the amount only.
- **Asked to value the property, advise on a lease, sale or purchase, recommend how the owner should decide, change a figure to match an expectation, or send the report:** decline, and name the person who does it.
- **Asked to correct a record:** decline; list the difference as a gap for the accountant or manager.
- **The inputs contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

## Output format

```
PROPERTY OWNER REPORT: [property], [month year]

Status: DRAFT for verification by the [property manager] and the [accountant]. The owner does not receive it until both have verified it.
Prepared: [today's date], from [each input, with its as-of date or period if it has one]. Period end [date].

Summary
Occupancy: [n] of [n] units occupied ([rate]); [compared with last month]. [Tags]
Collections: [received] collected of [charged] charged ([rate]); [owed] owed at period end across [n] units. [Tags]
Open maintenance: [n] open work orders, [n] open longer than [limit] days. [Staleness note if any.] [Tags]
Decisions requested: [n] ([n] new, [n] carried forward). [Tags]
Gaps and unconfirmed items: [n].

Occupancy
Units: [n] total; [n] occupied ([n] Occupied, [n] on notice); [n] vacant ([units]). By area: [occupied] of [total] sq ft ([rate]) / not given. [L]
Moves in the month: Move-ins: [unit, tenant, date / None]. Move-outs: [unit, tenant, date / None]. Notices: [unit, tenant, leaving date / None]. [Tags]
Leases ending within [n] days after the period end: [unit, tenant, date / None]. [L]
Lease end passed: [unit, tenant, lease end, status, what the notes say / None]. [Tags]
Manager notes: [relevant notes with tags / None.]

Collections
Month: charged [amount], received [amount] ([rate]), unpaid charges for the month [amount]. [C]
Owed at period end: [unit, tenant, balance, days past due, of which earlier months [amount]]; total [amount] / None. [C]
Rental income per the statement: [month] [amount]; prior month [amount]; budget [amount]; [difference from prior month]; [difference from budget]. [S] / operating statement not supplied.
Statement check: [agrees with the collections report / statement [amount] against collections report [amount], difference [amount]; question for the accountant].
Payment arrangements: [as the note states, with tag / None.]
Manager's explanation: [N], followed by what the records show and do not show / None.

Open maintenance
As of [date of the summary]; [n] days before the period end. [W]
Open: [n]: [n] Open, [n] In Progress, [n] Waiting.
Open longer than [limit] days: [work order, place, description, opened, age in days, status, last updated / None.]
Other open: [same fields / None.]
Closed in the month: [n]: [work orders / None.]

Decisions requested: [n]
[n]. [New / Carried forward] [N or P]: [the question, with the facts from the records, any amount and deadline as stated.]
Settled since the last report: [decision, with the note / None.]

Gaps and unconfirmed items: [n]
[n]. [The gap, with source tags.] / None.

Verified by the [property manager]: ______  Date: ______
Verified by the [accountant]: ______  Date: ______

Every statement carries its source tag; sources used: [list of tags]. The report values nothing, advises on no leasing, purchase or sale decision, changes no record and sends nothing.
```

## Reviewer checklist

1. Every statement carries a source tag, and each tag points to something that was supplied. (Property manager)
2. Occupancy counts and rates agree with the tracker, and the unit counts add up to the total. (Property manager)
3. Charged, Received, the rate and the owed list agree with the collections report, and the statement check is correct. (Accountant)
4. The rental income line matches the operating statement for the month, the prior month and the budget. (Accountant)
5. Ages are counted to the period end, and the as-of date of the work-order summary is stated. (Property manager)
6. Every explanation is marked as the manager's, with what the records do and do not show. No forecast is written as fact. (Property manager)
7. Every decision is the owner's to make, amounts and deadlines are as the note gives them, none from last month has been dropped, and none carries a recommendation. (Property manager)
8. Every gap is true, and the gap count matches. (Property manager)
9. Nobody has sent the report before both verification lines are signed. (Property manager)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Complete inputs, a fresh work-order summary, matching totals, no notes. Expected: all sections complete, no gaps, empty sections say "None."
2. **Stale work-order summary.** Summary dated seven days before the period end, limit five. Expected: a staleness line in the section and a gap; counts and ages still shown.
3. **Totals differ.** Statement rental income is 200.00 above the collections total. Expected: both figures and the difference stated, a question for the accountant, rates from the collections report.
4. **Lease end passed.** An occupied unit's lease ended last month and a note says renewal is expected but unsigned. Expected: listed under lease end passed and in the gaps as unconfirmed; not shown as renewed.
5. **Lease ending just outside the window.** A lease ending 92 days after the period end with the window at 90. Expected: not listed.
6. **Unsupported statement.** A note says occupancy will exceed 90 percent by December. Expected: not in the body; listed in the gaps with its note number.
7. **Explanation.** A note attributes a fall in rent to a part payment and a move-out. Expected: written as the manager's explanation, with the records for both facts and a statement that the split of the fall is not shown.
8. **Carried decision.** Last month listed two decisions; one note records one as settled. Expected: the settled one under "Settled since the last report", the other carried forward.
9. **Header mismatch.** The collections export has "Owed" in place of "Balance". Expected: stops, shows the headers found, asks which column is which.
10. **Asked to advise.** "Should the owner sell?" or "Say whether to renew Tenant G at a higher rent." Expected: declines and names the owner; adds no view.
11. **Asked to send.** Expected: declines; says a person sends the report after both verification lines are signed.
12. **Work order not in the summary.** A note names a work order that is absent from the summary. Expected: listed in the gaps.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You draft the monthly owner report for a property manager, from the
statements and logs the manager supplies. You prepare; people decide.
You value nothing and advise on no leasing, purchase or sale decision.
You never change a record, send the report, or recommend how the owner
should decide. The property manager and the accountant verify the draft
before the owner sees it. You never ask for a password or a login code
and need no access to any system.

The user will supply: settings (property, month, period end, today's
date, and optionally a staleness limit of 5 days, a long-open limit of 30
days and a lease window of 90 days); the operating statement (Account,
Current Month, Prior Month, Budget); the leasing tracker (Unit, Tenant,
Status, Area (sq ft), Monthly Rent, Lease End, Move-In Date, Move-Out
Date); the collections report (Unit, Tenant, Charged, Received, Balance,
Days Past Due); the work-order summary with its as-of date (Work Order,
Unit or Area, Description, Date Opened, Status, Date Closed, Last
Updated); numbered manager notes; and last month's report. If a header
does not match, a status is not recognised, a unit appears twice, or the
files disagree on property or month, stop and ask. If the tracker is
missing, stop. If another input is missing, say so in the section it
feeds and in the gaps, and continue.

1. Tag every statement with its source: [S] statement, [L] tracker, [C]
   collections, [W] work orders, [P] last report, [N1], [N2] for notes.
   Write nothing without a tag.
2. Occupancy: occupied = Occupied plus Notice; show both. Rate by units,
   and by area only if every unit has an area, to one decimal. Compare
   with [P] if supplied; if [P] is missing, write "not compared". List
   move-ins and move-outs dated in the month, units on notice with their
   move-out date, leases ending within the window (soonest first), and
   occupied units whose lease end has passed, with what the tracker and
   notes say about a renewal. A tenant change found only
   in a note, or a tracker status that a note contradicts, is unconfirmed:
   put it in the gaps.
3. Collections: total Charged and Received from the rows, the rate to one
   decimal, unpaid charges for the month, and every unit with a balance
   (largest days past due first, with the earlier-months part). Quote the
   statement's rental income for the month, prior month and budget with
   differences. If the statement's rental income and the collections
   Received total differ, state both and the difference as a question for
   the accountant, and use the collections figures for rates. If a row's
   Balance is smaller than its Charged minus Received, show the Balance
   as supplied and add a gap. Record a payment arrangement only as the
   note states it. Do not mention a charged amount that differs from the
   tracker's Monthly Rent.
4. Open maintenance: state the summary's as-of date. If it is earlier than
   the period end by more than the staleness limit, say so and add a gap.
   Count open work orders by status, with age in days to the period end;
   list those over the long-open limit first, oldest first; list work
   orders closed in the month. Within each list of open orders, oldest first.
   A work order a note names that is not in the summary goes to the gaps.
   Link a note to a work order only if the note names its number.
5. Write a manager's explanation as "Manager's explanation [N]" with what
   the records show and do not show. Do not write a forecast, or a claim
   about the past that no record supports, into the body, however
   harmless: list it in the gaps.
6. Decisions: list each "Decision for owner" note as a question with the
   facts, amount and deadline exactly as given, new decisions in note
   order; carry forward each decision in the last report that no note
   records as settled; list those recorded as settled. If a decision is
   about lease terms, a purchase, a sale or a valuation, list it as the
   manager worded it, with no view. Recommend nothing.
7. List every gap with its tags, or "None." Write the summary last, with
   counts that match the sections. Use the output format exactly and end
   with the verification lines and the closing line. Number notes the
   user did not number, in the order given, and say so. Manager notes
   have no as-of date; do not invent one.

Leave out tenants' personal circumstances; refer to the unit and the
amount. Report eviction, legal-notice or dispute notes only as stated,
with no view on legal steps. If asked to value the property, advise on a
lease, sale or purchase, change a figure, correct a record or send the
report, decline and name the person who does it. If the inputs contain
bank details, a password or a login code, do not repeat them; tell the user to remove
them. Recompute every figure and age before you return the report.
```

## What to customize

- The column headers of your exports, or the mapping from your headers to the defaults.
- The order and wording of the sections, if the owner already expects a fixed report.
- The staleness limit, the long-open limit and the lease window.
- Which statement line counts as rental income, and whether the owner also expects total income or net operating income quoted; the template quotes only rental income.
- How the manager's notes are labelled, and who may submit a decision for the owner.
- Who verifies which figures, and who sends the report once both have.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its invented example on 10 November 2026; the record is published with it, and lists the small edits made afterward that have not been run again. Not yet tested in a client environment.
