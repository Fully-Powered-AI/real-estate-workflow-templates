# Unit turnover readiness checklist: one recorded run on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (the settings, the move-out record, the turnover checklist and the vendor and work updates). No client data was used. The run was done by an assistant that had not written the template. It read the member template and only the example's inputs, followed the instruction block and the output format, and produced the output below. Only then was the output compared with the published example's output.

## What came out

```
UNIT TURNOVER READINESS CHECKLIST: Quillon Yard Apartments, unit 4B

For: property manager. Prepared: Monday 14 December 2026. Move-out: Saturday 5
December 2026. Approved move-in: Saturday 19 December 2026. Needed by: Friday 18
December 2026 (4 days from today; 1 day before move-in).
Sources: move-out record (9 items); turnover checklist (10 items); vendor and work
updates (7 updates); settings. Defaults used: needed 1 day before move-in; an update is
old after 3 days.
Lines: 18 (8 repairs, 10 checklist items). Reported complete: 4. Open: 14. Flagged: 8.
Decisions: 9.
Readiness is for the property manager to decide after verifying the unit. This checklist
does not say the unit is ready.

1. REPAIRS FROM THE MOVE-OUT RECORD
R1 Kitchen: dishwasher does not drain. Noted 5 Dec. Open: booked for 16 Dec, vendor confirmed. Update V3, Vendor C (appliance repair), repair dishwasher drain; status booked, promised Wed 16 Dec, vendor confirmed yes, updated 12 Dec.
R2 Living room: carpet stained near the window. Noted 5 Dec. Open: booked for 21 Dec, vendor confirmed. Update V4, Vendor D (flooring), replace living room carpet section; status booked, promised Mon 21 Dec, vendor confirmed yes, updated 10 Dec. FLAG, promised after needed-by, update is old: promised 3 days after the needed-by date and 2 days after the move-in; the update is 4 days old. See decision 1.
R3 Bedroom: wall scuffs and nail holes. Noted 5 Dec. Reported complete: vendor confirmed. Update V1, Vendor A (painter), patch and repaint bedroom walls; status reported done, promised Fri 11 Dec, vendor confirmed yes, updated 11 Dec.
R4 Bathroom: tub caulk cracked. Noted 5 Dec. Open: reported done, completion not confirmed. Update V5, Vendor E (handyman), re-caulk tub; status reported done, promised Sun 13 Dec, vendor confirmed no, updated 13 Dec. FLAG, completion not confirmed. See decision 2.
R5 Bedroom: closet door off its track. Noted 5 Dec. Open: blocked. Update V6, Vendor E (handyman), rehang closet door; status blocked, promised Tue 15 Dec, vendor confirmed no, updated 13 Dec. Note: "No access: key not at the unit". FLAG, blocked. See decision 3.
R6 Hallway: smoke alarm chirping. Noted 5 Dec. Open: no work recorded. FLAG, no work recorded. See decision 4.
R7 Living room: blind has two bent slats. Noted 5 Dec. Open: condition unclear. FLAG, condition unclear. See decision 5.
R8 Bathroom: chip in tub enamel; former tenant says it was there at move-in. Noted 5 Dec. Open: condition record disputed. FLAG, condition record disputed. See decision 6.
No repair needed: R9 Kitchen, cabinet hinge tight but sound.

2. CLEANING
C1 Appliances cleaned inside and out. Open. Checklist status: not done, 13 Dec. No update covers it.
C2 Full turnover clean (floors, bathroom, kitchen). Open: booked for 17 Dec, vendor not confirmed. Update V2, Vendor B (cleaner), full turnover clean; status booked, promised Thu 17 Dec, vendor confirmed no, updated 9 Dec. FLAG, awaiting vendor confirmation, update is old: the update is 5 days old. See decision 7.

3. KEYS AND ACCESS
C3 Unit key set cut and tagged (2 sets). Reported complete. Checklist status: done, 12 Dec.
C4 Mailbox key and building fob programmed. Open. Checklist status: not done, 12 Dec. No update covers it.
C5 Locks rekeyed. Reported complete. Checklist status: done, 10 Dec.

4. UTILITIES
C6 Electricity moved to the owner's name from the move-out date. Reported complete. Checklist status: done, 8 Dec.
C7 Gas account moved to the owner's name from the move-out date. Open: status not supplied. FLAG, status not supplied. See decision 8.
C8 Water and trash set up for the incoming tenant. Open. Checklist status: not done, 12 Dec. No update covers it.

5. OTHER CHECKLIST ITEMS
C9 Photos of the unit taken for the file. Open. Checklist status: not done, 13 Dec. No update covers it.
C10 Property manager's walk-through of the unit. Open. Checklist status: not done, no date. No update covers it.

6. VENDOR CONFIRMATIONS STILL OUTSTANDING
V2 Vendor B (cleaner), full turnover clean, covers C2: booked date (Thu 17 Dec) not confirmed; updated 9 Dec.
V5 Vendor E (handyman), re-caulk tub, covers R4: completion not confirmed; updated 13 Dec.
V6 Vendor E (handyman), rehang closet door, covers R5: visit not confirmed (blocked); updated 13 Dec.
V7 Vendor B (cleaner), window cleaning, covers R10: booked date (Thu 17 Dec) not confirmed; updated 12 Dec. R10 is not on the record.

7. DECISIONS FOR THE PROPERTY MANAGER: 9
1. R2, promised after needed-by, update is old. Vendor D is booked for Mon 21 Dec, vendor confirmed; needed-by is Fri 18 Dec and move-in Sat 19 Dec; the last update was 10 Dec. Does the vendor have an earlier date, or will the needed-by or move-in date change? Is there a newer update?
2. R4, completion not confirmed. Vendor E reported the re-caulk done on 13 Dec; completion is not confirmed. Has the vendor or the manager confirmed the work is complete?
3. R5, blocked. The visit is blocked: "No access: key not at the unit". What is blocking it, and who clears it before Fri 18 Dec?
4. R6, no work recorded. The smoke alarm finding has no update. Is work booked? If so, which vendor and what date?
5. R7, condition unclear. Does the record need to say repair or no repair?
6. R8, condition record disputed. The record notes a chip in the tub enamel and that it is disputed. Which record does the manager treat as current for this turnover? This checklist takes no side.
7. C2, awaiting vendor confirmation, update is old. Booked for Thu 17 Dec; not confirmed; last update 9 Dec. Has the vendor confirmed? If not, who asks, and by when? Is there a newer update?
8. C7, status not supplied. What is the status of the gas account item?
9. V7, unmatched update. Vendor B is booked for window cleaning on Thu 17 Dec, covering R10, which is in neither file. Should the finding be added to the record, or does the update belong to another item?

8. THINGS TO CHECK
- R6 (move-out record, finding): uses the words "smoke alarm". This checklist does not assess it. Who looks at it, and when?

9. DRAFT MESSAGE TO THE INCOMING TENANT
HOLD: not for sending until the property manager has verified the unit and approved this message.
Hello,
Your move-in at Quillon Yard Apartments, unit 4B, is Saturday 19 December 2026. Keys will be handed over at 10:00 at the leasing office. If you have a question before then, please contact the leasing office.

Draft for the property manager. Nothing has been verified, booked, sent or changed. This checklist certifies nothing about the unit's habitability, safety or compliance with any code.
```

## What was observed

- **Every required part was produced.** All nine sections, the header counts and the closing line came out in the order of the output format. The assistant was not told to stop for anything: the headers matched, the move-in date was in the future, no ID repeated, no tie between updates, and no password or door code was in the inputs.
- **Counts agree with the published example:** 18 lines (8 repairs, 10 checklist items), 4 reported complete, 14 open, 8 flagged, 9 decisions, needed-by Friday 18 December 2026.
- **One real difference, and it was the assistant's slip.** On R8 (disputed, repair needed yes, no update) the first pass wrote only "condition record disputed". The published example also flags "no work recorded", which is what step 6 requires for any finding marked yes with no update. The template does say this, but the state rule for a disputed finding ("whatever else is recorded"; wording since changed) reads as if the dispute replaces the other facts, and that is how it was first read. The flagged-line count and the decision count were not affected, but the decision for R8 lacked the "is work booked" question. This is recorded as a place where a reader can go wrong.
- **Other differences from the example were wording only:** the example repeats the dates in the state text ("booked for 21 Dec, vendor confirmed"), writes the vendor-confirmation lines with the promised date and weekday, and words the decisions at more length. For V6 (blocked, not confirmed) the example says "not confirmed" and this run said "visit not confirmed (blocked)".
- **Ambiguities met, where the assistant had to choose:**
  1. A blocked update with `vendor_confirmed` no is listed under outstanding confirmations (step 7), but the template names only three things that can be unconfirmed (the booked date, the completion, the visit), and none fits a blocked visit cleanly. "Visit" was used.
  2. The message sentence in the output format has a place for the time and the place but not the handover day, although the day is a setting. Here the handover day equals the move-in day, so nothing was lost, but a different day would have no place to go.
  3. The safety words in step 9 are said to apply to findings and update notes. Checklist items and the checklist's note column are not mentioned. "Closet door off its track" and "tub caulk cracked" were not treated as safety words (a door that will not close or secure; a leak). A reader could take either view, and the example agrees with this run.
  4. The rule to refer to a finding by its ID only when a note names a tenant in a dispute does not say what to do when the finding text only mentions a role ("former tenant"). This run kept the finding's words, as supplied, without any name.
  5. "Blocked" updates are not covered by the "awaiting vendor confirmation" flag, which is limited to booked, in progress or not started. This run did not flag R5 for it. The example agrees.
- **Facts not in the inputs:** none found in this run's output. In the published example, every fact traced back to the inputs. The weekday names, the day counts and the observation that R10 is not on the record are all derived, and were checked by hand against the calendar.
- **Limits of this record.** It is one run, by one product, on invented data, with a reader who then checked it against the answer. It says nothing about how the template behaves on a real property manager's files or in another product.

## Edits made after this run, not run again

After an independent review, the template and the example were edited. The recorded output above is unchanged and was not repeated. The edits: the message wording now has a place for the handover day; the state rule for a disputed finding says the dispute is shown together with any other state that applies (the place where this run went wrong on R8); a blocked update is listed as "blocked: the visit"; the blocked question asks whether the cause in the note is still current; safety words now also apply to a checklist's note column, not to an item's standing text; and the example's header no longer says "Defaults used", because its settings supplied both values (the run's own header above says "Defaults used" because the settings it read still carried the label "(the default)"; the label has since been dropped from the example's settings). Later edits, also not run again: the safety-word rule now names an exterior or entry door, so a closet door is no longer ambiguous (ambiguity 3 above); a finding marked no and disputed yes is listed with "record disputed" and raises a question under things to check; the instruction block now names mold, the lockbox code rule and the rule for a note that names a tenant in a dispute; the example's decision for R8 now carries the "is work booked" question, which this run's R8 decision lacked; and the example's done checklist items now carry "No update covers it." like the open ones. Latest small edits, after the second review, also not run again: the order of the sentences in step 9 was corrected; the question for "no work recorded" in the instruction block now also asks for the date; the "condition record disputed" flag is stated to apply only to a finding that has a line; the vendor-confirmation lines in the example were reworded to one pattern; and the public profile was reworded. A second run has not been done. These changes have not been tried in a new run.
