# Property diligence index

Workflow template, version 0.1.0.

## Purpose

Keep a property transaction's data room in order. From four lists and a few settings, build an index of every document received, grouped by workstream, and a tracker of every checklist item, request and open item, each tied to the report or request that raised it. The assistant prepares the index from the fields supplied. It reads no report, values nothing, advises on no transaction or price, interprets no finding and says nothing about whether a property is sound. It contacts no one and changes no record. The transaction lead assigns follow-up, and qualified specialists judge the findings.

## When to use it and when not to

Use it when a diligence period opens and reports, requests and questions are arriving from several parties. Run it again whenever documents arrive, requests are answered or items are raised. It suits a purchase, a financing or a disposition where the file is a set of outside reports.

Do not use it to prepare evidence for an audit (use the audit evidence index), to compare bids or quotes (use the vendor quote comparison), to value a property or judge a price, or to say that a report is clear, a defect is minor or title is good. Do not use it to read a report and pull findings out of it: the findings come from the person, in the person's words.

## Roles

- **Runs it:** the transaction coordinator or the acquisitions lead.
- **Reviews the index, assigns follow-up, decides which specialist receives which finding and when anything is sent:** the transaction lead.
- **Owns each open item:** the person the transaction lead names.
- **Judges the findings:** qualified specialists, such as the inspector, the title company, the environmental consultant and the property's advisers.

## Inputs

Four lists, each with a header row, plus settings. The assistant expects these default headers and reads nothing else into them. If a header differs, is missing or is not recognised, it stops and asks which column is which before doing anything else.

1. **Diligence checklist.** Headers: `checklist_id`, `workstream`, `item_text`, `due_date`. Dates are year-month-day. A blank `due_date` prints as "no due date". If missing, stop.
2. **Request log.** Headers: `request_id`, `workstream`, `request_text`, `requested_on`, `requested_from`, `checklist_id`, `status`. Status is one of Open, Received or Withdrawn. A blank `checklist_id` means the request is not on the checklist. If missing, say so; every Requests list reads "Request log not supplied" and no checklist item can be shown as Requested, outstanding.
3. **Document list.** Headers: `doc_id`, `workstream`, `title`, `author`, `report_date`, `received_date`, `pages_stated`, `pages_received`, `request_id`, `checklist_id`. A blank date prints as "date not recorded". If missing, stop.
4. **Items raised.** Headers: `item_id`, `source_doc_id`, `source_request_id`, `page_ref`, `item_text`, `assigned_to`, `due_date`, `status`, `conflicts_with`. Status is one of Open, In progress or Closed. The `item_text` is the person's own wording; the assistant never rewrites it or adds to it. If missing, say so; every Open items list reads "Items not supplied".
5. **Settings.** The deal name, the property label, today's date, the date the diligence period ends (from the agreed timetable), the transaction lead's role, the chase-after days (default 5) and the due-soon window in days (default 5). If today's date or the end date is missing, stop.

## The procedure

1. **Check the inputs.** Confirm the headers, that every date is readable, that `checklist_id`, `request_id`, `doc_id` and `item_id` values are each unique, that each status is one of the allowed words, and that every `workstream` in the request log and the document list is spelled exactly as in the checklist. Stop on any failure (see the stop conditions). The workstream order is the order in which each first appears in the checklist.
2. **Count days in calendar days** between the dates as supplied. Do not adjust for weekends or holidays. Write "1 day" for one and "[n] days" for any other number.
3. **Raise flags on each document.** A flag is a question for a person, not a finding.
   Each flag has fixed wording, printed exactly as shown:
   - **Pages incomplete:** both page counts are given and `pages_received` is lower than `pages_stated`. Wording: "Pages incomplete: [n] missing".
   - **More pages than stated:** `pages_received` is higher than `pages_stated`. Wording: "More pages than stated: [n] more".
   - **Page count not stated:** `pages_stated` is blank. Wording: "Page count not stated".
   - **Two versions:** another document names the same `checklist_id`, both have a `report_date`, and the dates differ. Flag both documents and name the other. Wording: "Two versions of [checklist id]: [other doc id] is dated [date]". If there are more than two, name each other document, separated by semicolons. Two documents with the same checklist item and the same date are not flagged.
   - **Not on the checklist:** `checklist_id` is blank or is not in the checklist. Wording: "Not on the checklist: no checklist item named" when blank, or "Not on the checklist: [id] is not in the checklist".
   - **Request not in the log:** `request_id` is filled but is not in the request log. Wording: "Request not in the log: [request id]".
   - **Workstream differs from the checklist item:** `checklist_id` is in the checklist but that item sits in another workstream than the document's own `workstream`. Wording: "Workstream differs from the checklist item: [checklist id] is in [workstream]".
   A document whose `checklist_id` is blank or not in the checklist is still indexed in the workstream its own `workstream` column names, and its line reads "Answers no checklist item". A document is always indexed in the workstream its own column names; a request in the workstream its own column names.
4. **Give each checklist item one status.**
   - **Received:** at least one document names it and none of those documents carries a flag.
   - **Received, check first:** at least one document names it and at least one of those documents carries a flag.
   - **Requested, outstanding:** no document names it, and at least one request names it with status Open or Received.
   - **Not requested:** no document names it, and no request names it, or every request that names it is Withdrawn (say so).
   For Requested, outstanding and Not requested only, add the timing: Overdue by the number of days when the due date is before today; Due today; Due in the number of days when the due date falls within the due-soon window after today; nothing more otherwise. Received and Received, check first carry no timing. A document naming the item decides its status, whatever its requests say: an item with a document while its request is still Open is Received (or Received, check first), and the request line still shows Open with its days open.
5. **Status of each request.** An Open request shows the days open (today minus `requested_on`). If the days open exceed the chase-after days, it reads "chase due"; otherwise "within chase window". A Received or Withdrawn request shows only its status. A request with status Received that no document names in `request_id` gets the flag "Marked received, but no document names this request".
6. **Tie each item to its source.** An item is tied when exactly one of `source_doc_id` and `source_request_id` is filled and that identifier exists. It then belongs to the workstream of its source and shows the source, with `page_ref` when given. An item with both filled, neither filled, or an identifier that is not found is not tied: it goes to the separate list of items not tied to a source, with the reason. A document line lists, under Items raised, the items whose `source_doc_id` names it; a request line lists the items whose `source_request_id` names it; either shows "none" when there are none.
7. **Timing and order of items.** An item that is Open or In progress shows Overdue by the number of days when its due date is before today, Due today, or Due in the number of days within the due-soon window; a blank due date prints "No due date" and carries no timing. An item with a blank `assigned_to` prints "owner not assigned"; the assistant never picks an owner. Within a workstream, list open items with no owner first, then by earliest due date, blank dates last, then by `item_id`. Closed items are counted and not listed.
8. **Conflicting statements.** Where an item names another item in `conflicts_with`, list the pair once, however many rows name each other, citing both items and their sources. Do not compare or judge the statements. If the named item does not exist, list the item among the items not tied with the reason "conflicting item id not found".
9. **Count and tie out.** Count the checklist items in each status; the four counts must equal the number of checklist rows. Count documents, requests by status, and items by status, and how many are tied and not tied; tied plus not tied must equal the number of item rows.
10. **Decisions for the transaction lead.** List, in the fixed order of the output format, the ids behind each decision. Decision 1 lists every Open or In progress item with no owner, including items not tied to a source. Nothing is assigned, chased or sent.
11. **Close.** Print the closing paragraph. "Prepared for" prints the transaction lead setting exactly as given. Return the index to the person who started the work only.

## Exceptions and stop conditions

- **A required header is missing, renamed, or an unknown header appears:** stop and ask which column is which. Do not guess.
- **An id appears twice:** stop and name the duplicate rows.
- **A workstream is spelled differently from the checklist, or a status is not an allowed word:** stop, name the row and ask.
- **A date cannot be read, or today's date or the end date is missing:** stop.
- **A request or document names a checklist item that does not exist:** do not stop; treat it as not on the checklist and say so.
- **Asked to read a report and pull items or findings out of it:** decline. The items come from the person, in the person's words.
- **Asked to say a report is complete in content, a finding is minor, a risk is acceptable, title is clear or a property is fit to buy:** decline. State what is indexed and what is open, and leave the judgment to the specialists and the transaction lead.
- **Asked to value a property, advise on a price or a transaction, or interpret a report:** decline.
- **Asked to assign an owner, contact a party, chase a request, send the index or change a record or file:** decline. A person does that.

## Output format

```
PROPERTY DILIGENCE INDEX: [deal name], [property label]

Prepared for: [transaction lead]. Index as of [today]. Diligence period ends [end date], [n] days away (or "ended [n] days ago", or "ends today").

Count: Checklist [n] items: Received [n], Received, check first [n], Requested, outstanding [n], Not requested [n]. Tie-out: [n] + [n] + [n] + [n] = [n]. Documents [n]. Requests [n]: open [n], received [n], withdrawn [n]. Items raised [n]: open [n], in progress [n], closed [n]; tied to a source [n], not tied [n].

WORKSTREAM: [name]

Documents
  [doc id]: [title], [author], dated [date], received [date]. Pages [received] of [stated]. Answers [checklist id or "no checklist item"]. Request [request id or "none"]. Items raised: [item ids or "none"].
    Flags: [flags, one after another, in the wording fixed in step 3, each ending in a full stop] (or "None.")
  (or "None." when the workstream has no documents)

Checklist
  [checklist id]: [item text], [due [date] | no due date]. [Status]. [Timing, where the rules give one]
  (or "None.")

Requests
  [request id]: [request text], to [requested from], sent [date]. [Open [n] days, chase due | Open [n] days, within chase window | Received | Withdrawn]. [Checklist [id] | Not on checklist.] Items raised: [item ids or "none"]. [Flag, if any]
  (or "None.")

Open items
  [item id]: [item text]. Source [doc id, page ref | request id]. Assigned: [name or "owner not assigned"]. [Due [date] | No due date]. [Open | In progress]. [Timing, where the rules give one]
  Closed items not listed: [n].
  (or "None." above the closed count when there are no open items)

(repeat the block for every workstream, in checklist order)

Conflicting statements: [item id (source)] and [item id (source)], named by [item id]. A qualified specialist judges which is right; the index does not compare them. (or "None.")

Items not tied to a source: [item id]: [item text]. Assigned: [name or "owner not assigned"]. [Due [date] | No due date]. [Status]. Reason: [no source named | both a document and a request named | source id not found | conflicting item id not found]. (or "None.")

Decisions for the transaction lead
1. Owners to assign: [open item ids with no owner, including items not tied to a source]. (or "None.")
2. Requests to chase, if a person chooses to: [request id (requested from)]. (or "None.")
3. Checklist items not yet requested: [checklist ids]. (or "None.")
4. Documents with flags to check: [doc ids]. (or "None.")
5. Conflicting statements to put to a qualified specialist: [item ids]. (or "None.")
6. Items not tied to a source, to link or drop: [item ids]. (or "None.")
7. Which qualified specialist judges each open finding, and what follow-up is assigned.

This index, built from the lists supplied for [deal name], shows what has been received, requested and raised, and where each open item came from. It does not show that a report is complete in content, that any finding is resolved, or what a property is worth. Qualified specialists judge the findings and the transaction lead decides the follow-up. The index changes no records and sends nothing.
```

Write dates as day, month name, year. In the Count line, "Received, check first" is a status name; keep its comma.

## Reviewer checklist

1. The tie-out adds up and matches the number of rows in the checklist. (Transaction lead)
2. Every workstream appears once, in checklist order. (Transaction lead)
3. Each document line matches the document list: dates, page counts, checklist item and request. (Transaction coordinator)
4. Each flag is supported by the supplied fields, and no flag is presented as a finding. (Transaction lead)
5. Each open item names a source that exists, and the item text is the person's wording unchanged. (Acquisitions lead)
6. No item has been given an owner by the assistant. (Transaction lead)
7. Days open, overdue and due-in counts are right for today's date. (Transaction coordinator)
8. Nothing in the index says complete, clear, acceptable, minor or fit, and nothing values the property. (Transaction lead)
9. The reports themselves have been opened by the specialists who judge them. (Specialists)

## Acceptance tests

Proposed tests. None has been run as a test in its own right. The invented example exercises tests 1 to 5, 8, 10 and 11 in effect; the trial record says what it showed.

1. **Clean document.** A document with matching page counts, a checklist item and a request, no other version. Expected: no flags; checklist item Received; no timing.
2. **Missing pages.** Stated 14, received 12. Expected: Pages incomplete, 2 missing; checklist item Received, check first.
3. **Two versions.** Two documents on one checklist item with different report dates. Expected: both flagged and each names the other; the item is Received, check first.
4. **Same date twice.** Two documents on one checklist item with the same report date. Expected: no Two versions flag.
5. **Requested, not received.** An Open request, no document. Expected: Requested, outstanding, with overdue or due-in timing; the request shows days open and chase due once past the chase-after days.
6. **Marked received, no document.** A Received request no document names. Expected: the flag on the request; the checklist item shows Requested, outstanding.
7. **Withdrawn only.** Every request for an item is Withdrawn. Expected: Not requested, and the withdrawal is mentioned.
8. **Item with no source.** Both source columns blank. Expected: listed among items not tied, with the reason; counted as not tied.
9. **Item with two sources.** Both filled. Expected: not tied, reason given.
10. **Conflict named from one side.** One item names the other in `conflicts_with`. Expected: the pair listed once, both items cited, neither statement compared.
11. **No owner.** A blank `assigned_to`. Expected: "owner not assigned", listed first in its workstream; the assistant proposes no owner.
12. **Workstream misspelled.** A document says "Title & survey" where the checklist says "Title and survey". Expected: stops and asks.
13. **Header changed.** A column renamed. Expected: stops and asks.
14. **Asked if the file is clean.** "Is the diligence file ready for closing?" Expected: declines to judge; states what is indexed and what is open.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a property diligence index for the transaction lead. You
index what has been received, requested and raised in a property
transaction, and you tie each open item to the report or request that
raised it. You never read or interpret a report, never value a property,
never advise on a transaction or price, never say a finding is resolved,
minor or acceptable, never assign an owner, and never contact anyone or
send, change or move a record or file. A person approves anything that
is sent or changed; qualified specialists judge the findings and the
transaction lead decides the follow-up.

The user will supply four lists with header rows and settings. Expected
headers: checklist checklist_id, workstream, item_text, due_date;
requests request_id, workstream, request_text, requested_on,
requested_from, checklist_id, status (Open, Received, Withdrawn);
documents doc_id, workstream, title, author, report_date, received_date,
pages_stated, pages_received, request_id, checklist_id; items item_id,
source_doc_id, source_request_id, page_ref, item_text, assigned_to,
due_date, status (Open, In progress, Closed), conflicts_with. Settings:
deal name, property label, today, diligence end date, transaction lead,
chase-after days (default 5), due-soon window days (default 5). If a
header differs or is missing, stop and ask which column is which. If the
checklist, the document list, today or the end date is missing, stop.
Stop on a duplicate id, an unreadable date, a status that is not an
allowed word, or a workstream not spelled as in the checklist. If the
request log is missing, write "Request log not supplied". If the items
list is missing, write "Items not supplied". Use item_text exactly as
given.

1. Count calendar days only. Workstream order is the order of first
   appearance in the checklist.
2. Flag documents, in this exact wording: "Pages incomplete: [n]
   missing" (both counts given, received below stated); "More pages than
   stated: [n] more" (received above stated); "Page count not stated"
   (pages_stated blank); "Two versions of [checklist id]: [other doc id]
   is dated [date]" (same checklist_id, both dated, dates differ; flag
   both and name the other, naming each other document if there are more
   than two, separated by semicolons; equal dates are not flagged); "Not
   on the checklist: no checklist item named" (blank checklist_id) or
   "Not on the checklist: [id] is not in the checklist"; "Request not in
   the log: [request id]" (request_id filled but not in the request
   log); "Workstream differs from the checklist item: [checklist id] is
   in [workstream]". Each flag ends in a full stop. A document is indexed
   in the workstream its own workstream column names, and a request in
   the workstream its own column names. A document with no checklist
   item reads "Answers no checklist item".
3. Checklist status: Received (a document names it, none flagged);
   Received, check first (a document names it, one flagged); Requested,
   outstanding (no document, a request Open or Received); Not requested
   (otherwise; mention withdrawn requests). A document decides the
   status even when its request is still Open; the request line still
   shows Open. Only Requested, outstanding and Not requested carry
   timing: Overdue by n days, Due today, or Due in n days inside the
   window. Write "1 day" for one, "n days" otherwise.
4. Requests: Open shows days open and "chase due" when days exceed the
   chase-after days, else "within chase window". A Received request that
   no document names gets the flag "Marked received, but no document
   names this request".
5. An item is tied only when exactly one of source_doc_id and
   source_request_id is filled and exists; it joins that source's
   workstream. Anything else goes to items not tied, with the reason.
   Open and In progress items show timing as above; blank due date
   prints "No due date"; blank assigned_to prints "owner not assigned".
   Order open items: no owner first, then earliest due date (blank dates
   last), then item_id. Closed items are only counted.
6. List a conflicting pair once if either item names the other. Never
   compare the statements. If a conflicts_with id is not found, send
   that item to the not-tied list with the reason "conflicting item id
   not found".
7. The four checklist status counts must equal the checklist rows; tied
   plus not tied must equal the item rows.
8. Use the output format exactly, with dates as day, month name, year.
   Each request line ends its facts with "Items raised:" and the ids of
   items that name that request, or "none". Print "None." for an empty
   list. Print the decisions in the fixed order, each ending in a full
   stop; decision 1 includes open items with no owner that are not tied
   to a source. Print the closing paragraph, and the transaction lead
   setting exactly as given. For the ended or ends-today forms of the
   period end, use "ended [n] days ago" or "ends today".

Use only the supplied fields. If asked whether the file is clean, a
finding is minor, a report is complete or a property is worth buying,
decline and report what is indexed and what is open.
```

## What to customize

- Your workstreams, spelled once and used identically in every list.
- The four exports and their column names, so each deal starts from the same files.
- The chase-after days and the due-soon window.
- The statuses you use for requests and items, if they differ from the three each.
- Which specialist judges which kind of finding, and who may assign follow-up.
- How the approved index reaches the deal team, and who sends it.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI from its own published map of the work. Tried on its invented example on 10 November 2026 in Claude, in one run; the record is published with it. Not yet tested in a client environment.
