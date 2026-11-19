# Transaction deadline check

Workflow template, version 0.1.0.

## Purpose

Read the brokerage's open-transactions export once a week, and whenever a contract is amended, and return one page for the transaction coordinator or managing broker: the milestones due in the brokerage's window, by agent; the milestones whose recorded date has passed with no completion recorded; transactions with a missing or impossible date; what changed since last week's export; and the questions to put to each agent. A count proves every open transaction and every tracked milestone was read. The assistant reads each date exactly as the export records it. It never works out a deadline from a contract, a statute or a business-day rule, gives no legal advice, contacts nobody, extends nothing and changes no record. The contract and the managing broker govern every deadline.

## When to use it and when not to

Use it every Monday on the week's export, and again on any day a contract is amended and the new dates have been entered in the transaction system. It suits residential and commercial brokerages alike, and any team that records milestone dates per transaction in one system.

Do not use it:

- to count a deadline from a contract's terms, a statute, a local custom or a rule about weekends and holidays. Someone who has read the contract enters the date; the check reads it;
- to decide whether a deadline has been met, missed, waived or extended in law, or what happens if it was missed. That is for the managing broker and, where needed, the client's lawyer. It gives no legal advice;
- to write an amendment, an extension or a notice to the other side;
- to message agents, clients, lenders or title and escrow officers. The coordinator decides who is asked what;
- when the export has not been refreshed since the last run: the page would only repeat last week.

## Roles

- **Runs it and supplies the export:** the transaction coordinator, or the managing broker where the brokerage has no coordinator.
- **Reads the page and decides what is chased, and by whom:** the transaction coordinator.
- **Answers the questions and updates the record:** the agent on each transaction, through the brokerage's own system.
- **Decides on any deadline that is in doubt:** the managing broker, with the contract in hand. Never the assistant.

## Inputs

1. **The open-transactions export from your real estate CRM or transaction system,** one row per open transaction, with these default column headers: `transaction_id`, `property`, `side`, `agent`, `acceptance_date`, then a date column and a completed column for each milestone the brokerage tracks. The default milestone columns are `deposit_due` and `deposit_completed`, `inspection_end` and `inspection_completed`, `financing_date` and `financing_completed`, `appraisal_date` and `appraisal_completed`, `title_date` and `title_completed`, `closing_date` and `closing_completed`. A date column holds the date as the brokerage recorded it, or `n/a` where the milestone does not apply to that transaction. A completed column holds the date the milestone was completed, or is blank. If the export is missing, stop and ask.
2. **Today's date.** If it is not given, stop and ask; never take it from the export's file name.
3. **The brokerage's settings:** the milestones it tracks, each with its display name, its date column and its completed column; how many days ahead counts as due soon (the window); who the page is for; the brokerage's name. Defaults: the six milestones above, in that order; a window of 7 calendar days; the page is for the transaction coordinator. Say which defaults were used; a setting that happens to equal a default counts as supplied, not as a default used, so say "none" when every setting was given.
4. **Last week's export,** optional, with the same headers. If it is not supplied, print "Last week's export not supplied" under Changes since last week.

**Column headers.** If a header in the export does not match the default or the brokerage's milestone list (missing, renamed or extra), stop and ask which column holds what. Never guess a column.

**What does not belong in the export.** Buyers' and tenants' personal finances (income, credit, loan amounts, bank details) and anything about a person's protected characteristics under fair-housing law are not needed and must be left out of the export before it is supplied. If a column or value appears to hold them, stop, do not repeat the value, and ask for the export again without it. The `property` column holds the address or a short label, not a client's name.

The assistant works from the files and notes supplied. It needs no connection to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm every header. Count the rows. If two rows share a `transaction_id`, stop and ask. Dates must be in one consistent format; if a date could be read two ways (03/04/2026), stop and ask which format the export uses.
2. **Set the window.** Window end = today + [your window] calendar days. A milestone is due in the window when its date is on or after today and on or before the window end. Count calendar days only. Never move a date for a weekend or a holiday, and never add or subtract days to a recorded date.
3. **Place every tracked milestone of every transaction in exactly one group,** testing in this order:
   1. **Not applicable:** the date column reads `n/a`, even where a completed date is recorded beside it; the completed value is not read for that milestone.
   2. **Date problem** (the after-closing test is skipped for a transaction whose closing date is itself a problem): the date is blank (missing) or unreadable; or the date is earlier than `acceptance_date`; or the completed value is unreadable, later than today, or earlier than `acceptance_date`; or, when the closing date is readable and not itself a problem, a milestone other than closing is dated after the closing date.
   3. **Completed:** a completed date is recorded.
   4. **Past, no completion recorded:** the date is before today.
   5. **Due in the window:** the date is from today to the window end.
   6. **Later:** the date is after the window end.
4. **Check each transaction as a whole.** A blank or unreadable `acceptance_date` is a date problem for the transaction (the before-acceptance tests are then skipped for it). A blank `agent` is listed as "agent not recorded", and that transaction's questions go to the person the page is for.
5. **Compare with last week's export,** if supplied, by `transaction_id`: transactions new this week; transactions no longer in the export (say only that they are gone; never guess whether they closed or fell through); every milestone date that changed, from and to; every completion recorded since last week; every completion that was recorded last week and is now blank.
6. **Write the questions,** grouped by agent, in transaction order and then milestone order. One question for each: milestone past with no completion recorded; date problem; milestone date changed since last week; completion removed since last week; transaction no longer in the export (to the agent last recorded on it). A milestone due in the window gets no question; it is listed for the agent's attention. Each question states the facts as recorded and asks what the transaction file shows. It never suggests a new date, a remedy or what the contract allows.
7. **Prove the count.** Transactions read = rows in the export. Transactions with something due, past or wrong + transactions with nothing due, past or wrong = transactions read, and the second group is listed by ID. Milestones read = transactions × tracked milestones = completed + due in the window + past with no completion + date problems + not applicable + later. If any count does not add up, stop and report the figures; print nothing else.
8. **Return the page** in the output format to the person who started the run. Do not send it onward.

## Exceptions and stop conditions

- **A header is missing, renamed or extra; a date is ambiguous; two rows share an ID; today's date is missing:** stop and ask.
- **The export appears to hold personal finances or anything about a person's protected characteristics:** stop; do not repeat it; ask for the export again without it.
- **The counts in step 7 do not add up:** stop and report the figures.
- **Asked to work out a deadline from the contract, a statute or a business-day rule, or to say whether a deadline was met, waived or extended:** decline; the managing broker decides with the contract in hand, and the page lists the recorded facts and the question.
- **Asked for legal advice, or to write an amendment, an extension or a notice:** decline; that is for the managing broker and the client's lawyer.
- **Asked to message an agent, a client or anyone else, or to update the transaction system:** decline; the transaction coordinator decides who is asked and the agent updates the record.

## Output format

```
TRANSACTION DEADLINE CHECK: [brokerage], as of [today, with weekday]

For: [transaction coordinator or managing broker]. Export: [n] open transactions. Last week's export: [n] transactions, or not supplied. Milestones tracked: [names, in order]. Window: [n] calendar days, through [window end]. Defaults used: [list, or none].

Read: Transactions read: [n] (rows in the export: [n]). With something due, past or wrong: [n]. With nothing due, past or wrong: [n] ([IDs]).
Milestones read: [n] ([transactions] x [milestones]). Completed: [n]. Due in the window: [n]. Past, no completion recorded: [n]. Date problems: [n]. Not applicable: [n]. Later: [n].

1. DUE IN THE WINDOW, BY AGENT: [n]
[Agent]
- [date] (in [n] days, or today): [milestone], [transaction_id], [property], [side].

2. PAST, NO COMPLETION RECORDED: [n]
- [date] ([n] days ago): [milestone], [transaction_id], [property], [agent].

3. MISSING OR IMPOSSIBLE DATES: [n] milestones; transaction fields: [n]
- [transaction_id], [property], [agent]: [milestone, or acceptance date or agent]: [what is recorded, exactly]; [the problem: missing, unreadable, before acceptance [date], completion after today, dated after closing [date], agent not recorded].

4. CHANGES SINCE LAST WEEK'S EXPORT ([date of last week's export])
New: [IDs].
No longer in the export: [IDs]. Why is not known from the export.
Dates changed: [transaction_id] [milestone]: [from] to [to].
Completions recorded: [transaction_id] [milestone]: [completed date].
Completions removed: [transaction_id] [milestone]: was [date], now blank.

5. QUESTIONS FOR EACH AGENT
[Agent, or "Agent not recorded: for the [role the page is for]"]
1. [transaction_id], [property]: [the facts as recorded]. [Question.]
Agents with no questions: [names].

Prepared for [role] to review. Every date is as recorded in the export; none was worked out from a contract, a statute or a business-day rule. Nothing has been sent, extended or changed. The contract and the managing broker govern every deadline.
```

Order within sections: section 1 by agent, then by date; section 2 by date, oldest first; section 3 by transaction, then milestone order. A completion listed in section 4 that is also a date problem in section 3 carries the pointer "(also in section 3)". One day away reads "in 1 day" and one day past reads "1 day ago". Section 3's heading counts milestone problems and, separately, transaction-level problems (an acceptance date or an agent that is blank); the lines below hold both kinds. Questions are numbered from 1 again under each agent, carry no "days ago" note, and ask only what the transaction file shows. An agent that is not recorded is listed in section 3 and the question goes to the reader of the page; no question asks who the agent is.

When a numbered section is empty, print "None." after its heading. When last week's export was not supplied, section 4 reads "Last week's export not supplied." and its lines are left out. A line under "Changes" that has nothing in it reads "None." Never leave a section out.

## Reviewer checklist

1. The headers matched the defaults or the brokerage's milestone list, or the mapping was confirmed. (Transaction coordinator)
2. Transactions read equals the rows in the export, and every transaction with nothing due, past or wrong is listed by ID. (Transaction coordinator)
3. The six milestone groups add up to transactions times tracked milestones. (Transaction coordinator)
4. Every date on the page matches the export exactly, and no date was moved or counted from a contract. (Transaction coordinator)
5. Every milestone past its recorded date with no completion has a question to its agent. (Transaction coordinator)
6. No question suggests a new date, a remedy or what the contract allows. (Managing broker)
7. No buyer's or tenant's personal finances or protected characteristics appear anywhere. (Managing broker)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean transaction.** Every milestone completed or later than the window. Expected: listed by ID under nothing due, past or wrong, and nowhere else.
2. **Past, no completion.** Financing date 2026-11-19, today 2026-11-23, completed blank. Expected: under section 2, "4 days ago", with a question to the agent.
3. **Last day of the window.** Window 7 days, today 2026-11-23, closing 2026-11-30. Expected: due in the window, "in 7 days".
4. **Closing before acceptance.** Acceptance 2026-11-10, closing 2026-11-05. Expected: date problem "before acceptance"; the after-closing test is skipped for that transaction.
5. **Missing date.** Financing date blank. Expected: date problem "missing", never treated as not applicable.
6. **Not applicable.** Financing date `n/a` on a cash purchase. Expected: counted as not applicable, no question.
7. **Completion in the future.** Completed 2026-12-02, today 2026-11-23. Expected: date problem "completion after today".
8. **Changed date.** Last week 2026-11-23, this week 2026-11-30. Expected: under Changes with both dates, and a question to the agent.
9. **Transaction gone.** In last week's export, not in this one. Expected: listed as no longer in the export with no guess at why, and a question to its last agent.
10. **Header mismatch.** `inspection_deadline` in place of `inspection_end`. Expected: stops and asks.
11. **Personal finances in the export.** A `loan_amount` column. Expected: stops, does not repeat the values, asks for the export without it.
12. **Asked to count the inspection period from the contract.** Expected: declines; the managing broker decides with the contract.

## Instructions for the AI assistant

```
You check a brokerage's open transactions for milestone dates, for the
transaction coordinator or managing broker. You read every date exactly
as the export records it. You never work out a deadline from a contract,
a statute or a weekend or holiday rule, and never move a date. You give
no legal advice. You never contact anyone, never extend anything and
never change a record; the coordinator decides who is asked and the
agent updates the system. You never ask for a password or a login code.

The user will supply: the open-transactions export from their real
estate CRM or transaction system; today's date; the brokerage's settings
(milestones tracked, each with its date column and completed column; the
window in days, default 7; who the page is for); optionally last week's
export. Default headers: transaction_id, property, side, agent,
acceptance_date, deposit_due, deposit_completed, inspection_end,
inspection_completed, financing_date, financing_completed,
appraisal_date, appraisal_completed, title_date, title_completed,
closing_date, closing_completed. A date column may read n/a. If a header
is missing, renamed or extra, a date could be read two ways, two rows
share an ID, or today's date is missing, stop and ask. If the export
seems to hold personal finances or protected characteristics, stop, do
not repeat them, and ask for the export without them.

1. Window end = today + window, in calendar days. Due in the window
   means on or after today and on or before the window end.
2. Put every tracked milestone of every transaction in one group,
   testing in order: not applicable (n/a); date problem (blank,
   unreadable, before acceptance_date, completed value unreadable or
   after today or before acceptance_date, or dated after a closing date
   that is itself sound); completed; past with no completion recorded;
   due in the window; later.
3. A blank or unreadable acceptance_date is a date problem for the
   transaction; skip the before-acceptance tests for it. A blank agent
   is "agent not recorded"; its questions go to the page's reader.
4. With last week's export, compare by transaction_id: new; no longer
   in the export (never guess why); dates changed, from and to;
   completions recorded; completions removed.
5. Questions by agent, one each for: past with no completion; date
   problem; date changed; completion removed; transaction gone. State
   the recorded facts and ask what the transaction file shows. Never
   suggest a date, a remedy or what the contract allows. Items due in
   the window get no question.
6. Prove the count: transactions read = rows; with something due, past
   or wrong + nothing due, past or wrong (listed by ID) = transactions
   read; milestones read = transactions x milestones = the six groups
   added. If a count fails, stop and report the figures.
7. Use the output format exactly, and follow the notes under it on
   line order, numbering under each agent, "in 1 day", "also in
   section 3" and what counts as a default used. Print "None." for
   an empty section. End with the closing line.

If asked to count a deadline, say whether one was met or extended, give
legal advice, write an amendment or notice, message anyone or update the
system, decline: the managing broker decides with the contract in hand.
```

## What to customize

- Your export's headers, or the mapping from them to the defaults.
- The milestones your brokerage tracks, their display names and their order, for residential and commercial work separately if they differ.
- [your window], the number of calendar days ahead that counts as due soon.
- Who the page is for: the transaction coordinator, the managing broker, or both.
- How your system marks a milestone that does not apply (the default is `n/a`).
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 19 November 2026. Written by FullyPowered AI. Tried on its example on 19 November 2026 in one run, published with it (`public/trial.md`). After that run the example's section 5 was edited to follow the output format (numbering restarts under each agent, no days-ago note, neutral questions, no question asking who the agent is), and the notes on ordering, "in 1 day", defaults and the after-closing test were added to the template; the instruction block was not changed at that point. Later the same day a reviewer's points were applied: the ordering note was made consistent, a pointer for a completion that is also a date problem was allowed, a clause was added for a completed date beside `n/a`, and one line in the instruction block now points to the notes under the output format. The instruction block's steps and the output format were not otherwise changed. None of these edits has been run again. Not yet tested in a client environment.
