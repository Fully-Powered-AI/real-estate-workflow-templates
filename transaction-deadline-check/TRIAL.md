# Transaction deadline check: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-19

The inputs are the invented example in [`example.md`](example.md): the settings, this week's export of eight open transactions and last week's export of eight. No client data was used. The run took the instruction block and the output format from the template and followed them as written. The page below was produced before the example's own page was read; the comparison came afterwards. One run, one product, one date: this shows the template can be followed on this example, not that it works for any brokerage's real export.

## What came out

```
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
```

## What was observed

- Every required part was produced: the header, the two count lines, all five numbered sections and the closing line. The counts added up on the first pass (16 + 6 + 3 + 3 + 4 + 16 = 48, and 6 + 2 = 8). The run stopped for nothing: all headers matched, no date was ambiguous, no ID repeated, today's date was given and the export held nothing it should not.
- Compared with the published example page, the counts, groups, dates, section 1, section 2, section 3 and section 4 are the same. Every fact in either page is in the inputs. No date was moved or worked out.
- Differences from the example, all in section 5 and in small matters of form:
  - The example adds a question to the page's reader asking who the agent is on T-106. The template's step 6 lists the questions to write and "agent not recorded" is not among them, so this run did not write one. The agent's absence is on the page in section 3.
  - The example's question about T-099 asks whether the transaction "has closed or ended". The template says never to guess whether a transaction closed or fell through. Asking is not guessing, but it nudges the agent toward two answers; this run asked only what the file shows.
  - The example's questions end "and is the record current?" or "or does this milestone not apply?" and give "(4 days ago)". This run used one plain question each and left out the days, since the template does not ask for them there.
  - The example numbers its questions 1 to 10 straight through; this run restarted at 1 under each agent. The template's format shows "1." under each agent.
  - This run printed "Prepared for transaction coordinator" word for word from the format; the example reads "the transaction coordinator".
- Where the instructions left room to guess:
  - Order of lines inside sections 1, 2 and 3 is not stated. This run used date order within each agent and in section 2, and transaction order in section 3; the example did the same.
  - Whether to list a completion that is also a date problem (T-106's deposit, dated after today) under "Completions recorded". The step says every completion recorded since last week; this run listed it and pointed to section 3.
  - Whether a date problem that is also a changed date (T-104's closing) gets one question or two. This run wrote two, one for each reason in step 6.
  - Section 3 counts "3 milestones; transaction fields: 1" but prints four lines. This is consistent with the template, and is easy to misread.
  - "Defaults used": the settings supplied matched the defaults exactly, so the run said "none". The template says to say which defaults were used and does not say whether settings that happen to equal the defaults count.
  - "In 1 day" versus "in 1 days": the format shows "[n] days" only. This run used the singular.
- Shortcomings of this trial: it is one run by one model on a small, tidy example. It did not exercise the stop conditions (the header, personal-finance and ambiguity cases in the acceptance tests), and nobody who runs a brokerage has checked the page against their own export.

## Edits made after this run

On 19 November 2026, after the run above, the published example's section 5 was changed to match what this run produced: numbering restarts under each agent, no days-ago note, plain questions, no question asking who the agent on T-106 is, and "Prepared for transaction coordinator". The template gained notes on line order, "in 1 day", defaults and the after-closing test; the instruction block was not changed at that point. Afterwards, when a reviewer's points were applied, the ordering note was made consistent (section 1 by agent then date, section 2 by date, section 3 by transaction then milestone), a pointer "(also in section 3)" was allowed for a completion that is also a date problem (the example now matches what this run wrote), a clause was added for a completed date beside `n/a`, and one line was added to the instruction block pointing to the notes under the output format. The recorded output above is untouched, and none of these edits has been run again.
