# Property diligence index: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example only: Quillfeather Property Group, Linden Court Apartments and every date, document and note in them are made up. No client data was used. This record replaces an earlier record of a first run made the same day, after an independent review asked for fixed flag wording, a "No due date" form, full stops on the decision lines and an Items raised field on request lines. The first run's output differed from the example in those places; the instructions were then changed, and this is a run of the changed instructions.

## Independence

The run was a single pass, but it was not independent. It was made by the same model session that edited the instructions, the output format and the example, and that had already read the first run's record and the example. It checks that the changed instructions can be followed to the example's result, and that the rules and the example now agree. It does not show that a model meeting the instructions cold would produce the same words.

## Inputs used

The five inputs in the [worked example](example.md): the settings, the diligence checklist (9 rows), the request log (8 rows), the document list (6 rows) and the items raised (9 rows).

## What came out

The index was produced by following the pasted instruction block and the output format, step by step. The whole output is below.

```
PROPERTY DILIGENCE INDEX: Linden Court purchase, Linden Court Apartments, 24 units

Prepared for: Acquisitions lead. Index as of 10 November 2026. Diligence period ends 20 November 2026, 10 days away.

Count: Checklist 9 items: Received 2, Received, check first 2, Requested, outstanding 3, Not requested 2. Tie-out: 2 + 2 + 3 + 2 = 9. Documents 6. Requests 8: open 4, received 4, withdrawn 0. Items raised 9: open 7, in progress 1, closed 1; tied to a source 8, not tied 1.

WORKSTREAM: Physical condition

Documents
  D01: Building inspection report, Inspector A, dated 3 November 2026, received 4 November 2026. Pages 62 of 62. Answers C01. Request Q01. Items raised: I01, I02.
    Flags: None.
  D02: Roof inspection report, Roofing contractor A, dated 2 November 2026, received 4 November 2026. Pages 12 of 14. Answers C02. Request Q02. Items raised: I03.
    Flags: Pages incomplete: 2 missing.

Checklist
  C01: Building inspection report, due 6 November 2026. Received.
  C02: Roof inspection report, due 6 November 2026. Received, check first.
  C03: Pest inspection report, due 13 November 2026. Not requested. Due in 3 days.

Requests
  Q01: Building inspection report, to Inspector A, sent 26 October 2026. Received. Checklist C01. Items raised: none.
  Q02: Roof inspection report, to Roofing contractor A, sent 26 October 2026. Received. Checklist C02. Items raised: none.

Open items
  I03: Photo schedule mentioned in the report is not in the pages received. Source D02, p. 6. Assigned: owner not assigned. Due 11 November 2026. Open. Due in 1 day.
  I02: Parking lot drainage noted; contractor estimate requested. Source D01, p. 31. Assigned: Property manager. Due 9 November 2026. In progress. Overdue by 1 day.
  I01: Further evaluation recommended for water staining in unit 7. Source D01, p. 14. Assigned: Property manager. Due 13 November 2026. Open. Due in 3 days.
  Closed items not listed: 0.

WORKSTREAM: Title and survey

Documents
  D03: Title commitment, Title agent A, dated 4 November 2026, received 5 November 2026. Pages 9 of 9. Answers C04. Request Q03. Items raised: I04, I05.
    Flags: None.

Checklist
  C04: Title commitment, due 6 November 2026. Received.
  C05: Documents listed as exceptions in the title commitment, due 9 November 2026. Requested, outstanding. Overdue by 1 day.
  C06: Boundary survey, due 13 November 2026. Not requested. Due in 3 days.

Requests
  Q03: Title commitment, to Title agent A, sent 26 October 2026. Received. Checklist C04. Items raised: none.
  Q04: Copies of the documents listed as exceptions, to Title agent A, sent 2 November 2026. Open 8 days, chase due. Checklist C05. Items raised: I06.

Open items
  I04: Commitment lists an easement exception; copy of the easement document requested. Source D03, Schedule B item 4. Assigned: Acquisitions lead. Due 12 November 2026. Open. Due in 2 days.
  I06: Exception documents not yet received; title review cannot finish. Source Q04. Assigned: Transaction coordinator. Due 12 November 2026. Open. Due in 2 days.
  Closed items not listed: 1.

WORKSTREAM: Environmental

Documents
  None.

Checklist
  C07: Phase I environmental report, due 13 November 2026. Requested, outstanding. Due in 3 days.

Requests
  Q08: Phase I environmental report, to Environmental consultant A, sent 28 October 2026. Open 13 days, chase due. Checklist C07. Items raised: none.

Open items
  None.
  Closed items not listed: 0.

WORKSTREAM: Seller records

Documents
  D04: Operating statements trailing twelve months, Seller's broker, dated 30 October 2026, received 30 October 2026. Pages 11 of 11. Answers C08. Request Q05. Items raised: I08.
    Flags: Two versions of C08: D05 is dated 5 November 2026.
  D05: Operating statements trailing twelve months, Seller's broker, dated 5 November 2026, received 5 November 2026. Pages 11 of 11. Answers C08. Request Q05. Items raised: I07.
    Flags: Two versions of C08: D04 is dated 30 October 2026.
  D06: Tenant ledger summary, Seller's broker, dated 6 November 2026, received 6 November 2026. Pages 3 of 3. Answers no checklist item. Request none. Items raised: none.
    Flags: Not on the checklist: no checklist item named.

Checklist
  C08: Trailing twelve-month operating statements, due 6 November 2026. Received, check first.
  C09: Service contract copies, due 13 November 2026. Requested, outstanding. Due in 3 days.

Requests
  Q05: Trailing twelve-month operating statements, to Seller's broker, sent 26 October 2026. Received. Checklist C08. Items raised: none.
  Q06: Service contract copies, to Seller's broker, sent 2 November 2026. Open 8 days, chase due. Checklist C09. Items raised: none.
  Q07: Written explanation of the difference between the two operating statements, to Seller's broker, sent 6 November 2026. Open 4 days, within chase window. Not on checklist. Items raised: none.

Open items
  I07: Total operating expenses differ from the earlier statement. Source D05, p. 2. Assigned: Acquisitions lead. Due 12 November 2026. Open. Due in 2 days.
  I08: Total operating expenses as shown in the earlier statement. Source D04, p. 2. Assigned: Acquisitions lead. Due 12 November 2026. Open. Due in 2 days.
  Closed items not listed: 0.

Conflicting statements: I07 (D05, p. 2) and I08 (D04, p. 2), named by I07. A qualified specialist judges which is right; the index does not compare them.

Items not tied to a source: I09: Ask seller about roof age. Assigned: owner not assigned. No due date. Open. Reason: no source named.

Decisions for the transaction lead
1. Owners to assign: I03, I09.
2. Requests to chase, if a person chooses to: Q04 (Title agent A), Q06 (Seller's broker), Q08 (Environmental consultant A).
3. Checklist items not yet requested: C03, C06.
4. Documents with flags to check: D02, D04, D05, D06.
5. Conflicting statements to put to a qualified specialist: I07, I08.
6. Items not tied to a source, to link or drop: I09.
7. Which qualified specialist judges each open finding, and what follow-up is assigned.

This index, built from the lists supplied for Linden Court purchase, shows what has been received, requested and raised, and where each open item came from. It does not show that a report is complete in content, that any finding is resolved, or what a property is worth. Qualified specialists judge the findings and the transaction lead decides the follow-up. The index changes no records and sends nothing.
```

## What was observed

- Every part of the output format was produced: the heading, the prepared-for line, the count line with its tie-out (2 + 2 + 3 + 2 = 9), all four workstreams in checklist order, the conflicting-statements line, the items not tied, the seven decisions and the closing paragraph. The tie-out and the item counts (8 tied plus 1 not tied = 9) added up.
- Nothing in the inputs triggered a stop condition. The headers, ids, statuses, workstream spellings and dates were all clean, so the stop rules were not exercised.
- No fact appeared in the output that was not in the inputs. Every date, count and number of days follows from the inputs and today's date.
- The output matches the published example line for line. That is expected here, because the example was brought into line with the changed rules first; it is not an independent confirmation.
- The points the first run found are now settled in the instructions and show in this output: flags use fixed wording; a blank due date reads "No due date"; decision lines end in a full stop; request lines carry an Items raised field, so I06 appears on request Q04 as well as under Open items; a document with a blank checklist id (D06) stays in the workstream it names and reads "Answers no checklist item".
- Places where the instructions still leave room to guess:
  - Decision 1, "open item ids with no owner", includes I09, which is not tied to a source. The text says "open items" without saying whether untied items count, so this was a choice. The example makes the same one.
  - The singular "1 day" and the plural "days" are not stated; the example uses "1 day".
  - The pasted instruction block shortens several rules. The longer procedure in the template was used to settle each doubt.
- Tests not exercised: the example exercises acceptance tests 1 to 5, 8, 10 and 11 in effect. Tests 6, 7, 9 and 12 to 14 (marked received with no document, withdrawn only, two sources, a misspelled workstream, a changed header, being asked if the file is clean) were not exercised.
- The template has not been run on messy or large lists, and nothing here says how it behaves with them.
- This is one run on an invented example. It shows the changed instructions can be followed to the example's result. It does not show how the template performs on a real deal, and it has not been tested in a client environment.

## Changes made to the instructions after this run

After an independent review, the instructions were edited again; this run was not repeated. The three places listed above where the instructions left room to guess were closed in writing: decision 1 now says it includes open items not tied to a source, "1 day" against "n days" is stated in the procedure and in the pasted block, and the pasted block now carries the conditions for the page-count flags, the workstream a document or request sits in, and the ended and ends-today forms. Two rules were added for cases the example does not contain (a document in a different workstream from its checklist item; a checklist item with a document while its request is still Open). The example inputs, the output format's layout and the output above did not change, so the output recorded here is still what that run produced, but the edited block has not been run. A fresh run of the pasted block by a session that did not write it would be stronger evidence and has not been made.
