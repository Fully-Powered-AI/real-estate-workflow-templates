# Property diligence index: an invented example

*Illustrative example with invented data.* The company, the property, the people and every document, date and note below are invented. Quillfeather Property Group is an invented company buying Linden Court Apartments, an invented 24-unit building. The acquisitions lead runs the capability and is also the transaction lead who reviews it. First come the inputs the acquisitions lead supplied, in full, then the index the capability returned. Today is Tuesday 10 November 2026.

## The inputs

### 1. Settings

```
Deal name: Linden Court purchase
Property label: Linden Court Apartments, 24 units
Today: 2026-11-10
Diligence period ends: 2026-11-20
Transaction lead: Acquisitions lead
Chase after: 5 days
Due-soon window: 5 days
```

### 2. Diligence checklist

```
checklist_id,workstream,item_text,due_date
C01,Physical condition,Building inspection report,2026-11-06
C02,Physical condition,Roof inspection report,2026-11-06
C03,Physical condition,Pest inspection report,2026-11-13
C04,Title and survey,Title commitment,2026-11-06
C05,Title and survey,Documents listed as exceptions in the title commitment,2026-11-09
C06,Title and survey,Boundary survey,2026-11-13
C07,Environmental,Phase I environmental report,2026-11-13
C08,Seller records,Trailing twelve-month operating statements,2026-11-06
C09,Seller records,Service contract copies,2026-11-13
```

### 3. Request log

```
request_id,workstream,request_text,requested_on,requested_from,checklist_id,status
Q01,Physical condition,Building inspection report,2026-10-26,Inspector A,C01,Received
Q02,Physical condition,Roof inspection report,2026-10-26,Roofing contractor A,C02,Received
Q03,Title and survey,Title commitment,2026-10-26,Title agent A,C04,Received
Q04,Title and survey,Copies of the documents listed as exceptions,2026-11-02,Title agent A,C05,Open
Q05,Seller records,Trailing twelve-month operating statements,2026-10-26,Seller's broker,C08,Received
Q06,Seller records,Service contract copies,2026-11-02,Seller's broker,C09,Open
Q07,Seller records,Written explanation of the difference between the two operating statements,2026-11-06,Seller's broker,,Open
Q08,Environmental,Phase I environmental report,2026-10-28,Environmental consultant A,C07,Open
```

### 4. Document list

```
doc_id,workstream,title,author,report_date,received_date,pages_stated,pages_received,request_id,checklist_id
D01,Physical condition,Building inspection report,Inspector A,2026-11-03,2026-11-04,62,62,Q01,C01
D02,Physical condition,Roof inspection report,Roofing contractor A,2026-11-02,2026-11-04,14,12,Q02,C02
D03,Title and survey,Title commitment,Title agent A,2026-11-04,2026-11-05,9,9,Q03,C04
D04,Seller records,Operating statements trailing twelve months,Seller's broker,2026-10-30,2026-10-30,11,11,Q05,C08
D05,Seller records,Operating statements trailing twelve months,Seller's broker,2026-11-05,2026-11-05,11,11,Q05,C08
D06,Seller records,Tenant ledger summary,Seller's broker,2026-11-06,2026-11-06,3,3,,
```

### 5. Items raised

```
item_id,source_doc_id,source_request_id,page_ref,item_text,assigned_to,due_date,status,conflicts_with
I01,D01,,p. 14,Further evaluation recommended for water staining in unit 7,Property manager,2026-11-13,Open,
I02,D01,,p. 31,Parking lot drainage noted; contractor estimate requested,Property manager,2026-11-09,In progress,
I03,D02,,p. 6,Photo schedule mentioned in the report is not in the pages received,,2026-11-11,Open,
I04,D03,,Schedule B item 4,Commitment lists an easement exception; copy of the easement document requested,Acquisitions lead,2026-11-12,Open,
I05,D03,,Cover page,Commitment effective date confirmed with Title agent A,Transaction coordinator,2026-11-09,Closed,
I06,,Q04,,Exception documents not yet received; title review cannot finish,Transaction coordinator,2026-11-12,Open,
I07,D05,,p. 2,Total operating expenses differ from the earlier statement,Acquisitions lead,2026-11-12,Open,I08
I08,D04,,p. 2,Total operating expenses as shown in the earlier statement,Acquisitions lead,2026-11-12,Open,
I09,,,,Ask seller about roof age,,,Open,
```

## The index

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

## How the figures were reached

- Checklist: C01 and C04 have an unflagged document, so Received (2). C02 has a document with missing pages and C08 has two versions, so Received, check first (2). C05, C07 and C09 have no document and an Open request, so Requested, outstanding (3). C03 and C06 have neither, so Not requested (2). 2 + 2 + 3 + 2 = 9 rows.
- Pages: D02 stated 14, received 12, so 2 missing.
- Days: today is 10 November. Q04 and Q06 were sent 2 November, 8 days; Q08 was sent 28 October, 13 days; Q07 was sent 6 November, 4 days. With a chase-after of 5 days, Q04, Q06 and Q08 are chase due and Q07 is within the window. C05 was due 9 November, 1 day overdue. C03, C06, C07 and C09 are due 13 November, in 3 days. I02 was due 9 November, 1 day overdue; I03 is due in 1 day; I04, I06, I07 and I08 are due in 2 days; I01 is due in 3 days. The end date, 20 November, is 10 days away.
- Items: nine rows. Open I01, I03, I04, I06, I07, I08, I09 (7); In progress I02 (1); Closed I05 (1). Eight name one existing source and one, I09, names none. I07 names I08, so the pair is listed once.
