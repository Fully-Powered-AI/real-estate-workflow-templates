# Transaction deadline check: an invented example

*Illustrative example with invented data.* Brokerage X is an invented brokerage with residential and commercial work. Its transaction coordinator runs the Monday check. The agents appear as letters, the properties are invented, and no buyer, seller or tenant is named. Every row and date below is invented.

The inputs come first, in full, so the workflow template can be run on them. The page follows.

## The inputs

### 1. Settings (typed by the transaction coordinator)

```
Brokerage: Brokerage X
Today: Monday 23 November 2026
Page is for: transaction coordinator
Milestones tracked, in order (display name: date column / completed column):
  Deposit due: deposit_due / deposit_completed
  Inspection period end: inspection_end / inspection_completed
  Financing date: financing_date / financing_completed
  Appraisal: appraisal_date / appraisal_completed
  Title: title_date / title_completed
  Closing: closing_date / closing_completed
Due soon: within 7 calendar days
Not applicable is marked: n/a
```

### 2. The open-transactions export from your real estate CRM or transaction system (this week, exported Monday 23 November 2026)

```
transaction_id,property,side,agent,acceptance_date,deposit_due,deposit_completed,inspection_end,inspection_completed,financing_date,financing_completed,appraisal_date,appraisal_completed,title_date,title_completed,closing_date,closing_completed
T-101,14 Alder Row,buyer,Agent A,2026-10-20,2026-10-23,2026-10-22,2026-10-30,2026-10-29,2026-11-19,,2026-11-12,2026-11-11,2026-11-25,,2026-12-01,
T-102,3 Birch Court,seller,Agent B,2026-11-02,2026-11-05,2026-11-05,2026-11-16,,2026-11-27,,2026-11-24,,2026-12-04,,2026-12-15,
T-103,Suite 4 at 220 Mill Street (office),buyer,Agent C,2026-09-28,2026-10-01,2026-09-30,2026-11-06,2026-11-05,n/a,,n/a,,2026-11-20,2026-11-18,2026-11-30,
T-104,9 Cedar Lane,both,Agent A,2026-11-10,2026-11-13,,2026-11-24,,,,2026-12-01,,2026-12-08,,2026-11-05,
T-105,61 Dune Road,buyer,Agent B,2026-10-26,2026-10-29,2026-10-28,2026-11-09,2026-11-09,2026-11-30,,2026-11-20,2026-11-19,2026-12-02,,2026-12-10,
T-106,Warehouse 2 at 5 Kiln Yard (industrial),seller,,2026-11-16,2026-11-19,2026-12-02,2026-12-07,,n/a,,n/a,,2026-12-14,,2027-01-08,
T-107,27 Elm Terrace,seller,Agent C,2026-11-18,2026-11-21,2026-11-20,2026-12-02,,2026-12-16,,2026-12-09,,2026-12-23,,2027-01-05,
T-108,8 Fern Close,buyer,Agent C,2026-10-05,2026-10-08,2026-10-08,2026-10-19,2026-10-17,2026-11-06,2026-11-05,2026-10-28,2026-10-27,2026-11-13,2026-11-12,2026-12-04,
```

The export holds no buyer, seller or tenant names, no personal finances and nothing about anyone's personal characteristics.

### 3. Last week's export (exported Monday 16 November 2026)

```
transaction_id,property,side,agent,acceptance_date,deposit_due,deposit_completed,inspection_end,inspection_completed,financing_date,financing_completed,appraisal_date,appraisal_completed,title_date,title_completed,closing_date,closing_completed
T-099,40 Gorse Hill,buyer,Agent B,2026-09-14,2026-09-17,2026-09-16,2026-09-28,2026-09-26,2026-10-16,2026-10-15,2026-10-09,2026-10-08,2026-11-06,2026-11-05,2026-11-13,2026-11-13
T-101,14 Alder Row,buyer,Agent A,2026-10-20,2026-10-23,2026-10-22,2026-10-30,2026-10-29,2026-11-19,,2026-11-12,2026-11-11,2026-11-25,,2026-12-01,
T-102,3 Birch Court,seller,Agent B,2026-11-02,2026-11-05,2026-11-05,2026-11-16,,2026-11-27,,2026-11-24,,2026-12-04,,2026-12-15,
T-103,Suite 4 at 220 Mill Street (office),buyer,Agent C,2026-09-28,2026-10-01,2026-09-30,2026-11-06,2026-11-05,n/a,,n/a,,2026-11-20,,2026-11-30,
T-104,9 Cedar Lane,both,Agent A,2026-11-10,2026-11-13,,2026-11-24,,,,2026-12-01,,2026-12-08,,2026-12-15,
T-105,61 Dune Road,buyer,Agent B,2026-10-26,2026-10-29,2026-10-28,2026-11-09,2026-11-09,2026-11-23,,2026-11-20,,2026-12-02,,2026-12-10,
T-106,Warehouse 2 at 5 Kiln Yard (industrial),seller,,2026-11-16,2026-11-19,,2026-12-07,,n/a,,n/a,,2026-12-14,,2027-01-08,
T-108,8 Fern Close,buyer,Agent C,2026-10-05,2026-10-08,2026-10-08,2026-10-19,2026-10-17,2026-11-06,2026-11-05,2026-10-28,2026-10-27,2026-11-13,2026-11-12,2026-12-04,
```

## The page

TRANSACTION DEADLINE CHECK: Brokerage X, as of Monday 23 November 2026

For: transaction coordinator. Export: 8 open transactions. Last week's export: 8 transactions. Milestones tracked: Deposit due, Inspection period end, Financing date, Appraisal, Title, Closing. Window: 7 calendar days, through 2026-11-30. Defaults used: none.

Read: Transactions read: 8 (rows in the export: 8). With something due, past or wrong: 6. With nothing due, past or wrong: 2 (T-107, T-108).
Milestones read: 48 (8 x 6). Completed: 16. Due in the window: 6. Past, no completion recorded: 3. Date problems: 3. Not applicable: 4. Later: 16.

1. DUE IN THE WINDOW, BY AGENT: 6

Agent A
- 2026-11-24 (in 1 day): Inspection period end, T-104, 9 Cedar Lane, both.
- 2026-11-25 (in 2 days): Title, T-101, 14 Alder Row, buyer.

Agent B
- 2026-11-24 (in 1 day): Appraisal, T-102, 3 Birch Court, seller.
- 2026-11-27 (in 4 days): Financing date, T-102, 3 Birch Court, seller.
- 2026-11-30 (in 7 days): Financing date, T-105, 61 Dune Road, buyer.

Agent C
- 2026-11-30 (in 7 days): Closing, T-103, Suite 4 at 220 Mill Street (office), buyer.

2. PAST, NO COMPLETION RECORDED: 3
- 2026-11-13 (10 days ago): Deposit due, T-104, 9 Cedar Lane, Agent A.
- 2026-11-16 (7 days ago): Inspection period end, T-102, 3 Birch Court, Agent B.
- 2026-11-19 (4 days ago): Financing date, T-101, 14 Alder Row, Agent A.

3. MISSING OR IMPOSSIBLE DATES: 3 milestones; transaction fields: 1
- T-104, 9 Cedar Lane, Agent A: Financing date: blank; missing.
- T-104, 9 Cedar Lane, Agent A: Closing: 2026-11-05; before acceptance 2026-11-10.
- T-106, Warehouse 2 at 5 Kiln Yard (industrial), agent not recorded: Deposit due: completed 2026-12-02; completion after today.
- T-106, Warehouse 2 at 5 Kiln Yard (industrial), agent not recorded: Agent: blank; agent not recorded.

4. CHANGES SINCE LAST WEEK'S EXPORT (2026-11-16)
New: T-107.
No longer in the export: T-099. Why is not known from the export.
Dates changed: T-104 Closing: 2026-12-15 to 2026-11-05. T-105 Financing date: 2026-11-23 to 2026-11-30.
Completions recorded: T-103 Title: 2026-11-18. T-105 Appraisal: 2026-11-19. T-106 Deposit due: 2026-12-02 (also in section 3).
Completions removed: None.

5. QUESTIONS FOR EACH AGENT

Agent A
1. T-101, 14 Alder Row: Financing date is recorded as 2026-11-19 with no completion recorded. What does the transaction file show?
2. T-104, 9 Cedar Lane: Deposit due is recorded as 2026-11-13 with no completion recorded. What does the transaction file show?
3. T-104, 9 Cedar Lane: Financing date is blank. What does the transaction file show?
4. T-104, 9 Cedar Lane: Closing is recorded as 2026-11-05, before the acceptance date of 2026-11-10. What does the transaction file show?
5. T-104, 9 Cedar Lane: Closing changed from 2026-12-15 to 2026-11-05 since last week. What does the transaction file show?

Agent B
1. T-099, 40 Gorse Hill: no longer in the export. What does the transaction file show?
2. T-102, 3 Birch Court: Inspection period end is recorded as 2026-11-16 with no completion recorded. What does the transaction file show?
3. T-105, 61 Dune Road: Financing date changed from 2026-11-23 to 2026-11-30 since last week. What does the transaction file show?

Agent not recorded: for the transaction coordinator
1. T-106, Warehouse 2 at 5 Kiln Yard (industrial): Deposit due completion is recorded as 2026-12-02, after today. What does the transaction file show?

Agents with no questions: Agent C.

Prepared for transaction coordinator to review. Every date is as recorded in the export; none was worked out from a contract, a statute or a business-day rule. Nothing has been sent, extended or changed. The contract and the managing broker govern every deadline.

## Checking the figures (not part of the page)

- Window end: 23 November + 7 days = 30 November 2026. Due in the window means 23 to 30 November inclusive.
- Milestones read: 8 transactions x 6 milestones = 48. Completed 16 (T-101: 3, T-102: 1, T-103: 3, T-105: 3, T-107: 1, T-108: 5). Due 6. Past 3. Date problems 3. Not applicable 4 (T-103 and T-106, financing and appraisal each). Later 16 (T-101: 1, T-102: 2, T-104: 2, T-105: 2, T-106: 3, T-107: 5, T-108: 1). 16 + 6 + 3 + 3 + 4 + 16 = 48.
- T-104's Appraisal (2026-12-01) and Title (2026-12-08) fall after its recorded closing, but its closing date is itself a problem, so the after-closing test is skipped for T-104 and both count as later.
- T-106 has no agent recorded, so its blank agent is listed in section 3 and its question goes to the transaction coordinator; no separate question asks who the agent is. Questions are numbered from 1 under each agent.
- T-107 and T-108 have only completed or later milestones, so they have nothing due, past or wrong. 6 + 2 = 8.
