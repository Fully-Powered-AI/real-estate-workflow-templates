# Unit turnover readiness checklist: an invented example

*Illustrative example with invented data.* The property, the unit, the vendors, the dates and every record below are invented. Quillon Yard Apartments is an invented 40-unit building. Its property manager runs the turnover of unit 4B between two tenants. Vendors appear as letters, and the incoming tenant is not named.

The inputs come first, in full, so the template can be run on them. The checklist follows.

## The inputs

### 1. Settings (typed by the property manager)

```
Property: Quillon Yard Apartments, unit 4B
Prepared for: property manager
Today: Monday 14 December 2026
Move-out date: Saturday 5 December 2026
Approved move-in date: Saturday 19 December 2026
Days before move-in the unit is needed: 1
Update counts as old after: 3 days
Message to the incoming tenant: yes
Key handover: Saturday 19 December 2026 at 10:00, at the leasing office
Contact named in the message: the leasing office
```

### 2. Move-out record

```
item_id,area,finding,repair_needed,disputed,noted_on
R1,Kitchen,Dishwasher does not drain,yes,no,2026-12-05
R2,Living room,Carpet stained near the window,yes,no,2026-12-05
R3,Bedroom,Wall scuffs and nail holes,yes,no,2026-12-05
R4,Bathroom,Tub caulk cracked,yes,no,2026-12-05
R5,Bedroom,Closet door off its track,yes,no,2026-12-05
R6,Hallway,Smoke alarm chirping,yes,no,2026-12-05
R7,Living room,Blind has two bent slats,unclear,no,2026-12-05
R8,Bathroom,"Chip in tub enamel; former tenant says it was there at move-in",yes,yes,2026-12-05
R9,Kitchen,Cabinet hinge tight but sound,no,no,2026-12-05
```

### 3. Turnover checklist, with status as of today

```
check_id,category,item,status,status_date,note
C1,cleaning,Appliances cleaned inside and out,not done,2026-12-13,
C2,cleaning,"Full turnover clean (floors, bathroom, kitchen)",not done,2026-12-13,
C3,keys,Unit key set cut and tagged (2 sets),done,2026-12-12,
C4,keys,Mailbox key and building fob programmed,not done,2026-12-12,
C5,keys,Locks rekeyed,done,2026-12-10,
C6,utilities,Electricity moved to the owner's name from the move-out date,done,2026-12-08,
C7,utilities,Gas account moved to the owner's name from the move-out date,,,
C8,utilities,Water and trash set up for the incoming tenant,not done,2026-12-12,
C9,other,Photos of the unit taken for the file,not done,2026-12-13,
C10,other,Property manager's walk-through of the unit,not done,,
```

### 4. Vendor and work updates

```
ref,vendor,work,covers,status,promised_date,vendor_confirmed,updated_on,note
V1,Vendor A (painter),Patch and repaint bedroom walls,R3,reported done,2026-12-11,yes,2026-12-11,
V2,Vendor B (cleaner),Full turnover clean,C2,booked,2026-12-17,no,2026-12-09,
V3,Vendor C (appliance repair),Repair dishwasher drain,R1,booked,2026-12-16,yes,2026-12-12,
V4,Vendor D (flooring),Replace living room carpet section,R2,booked,2026-12-21,yes,2026-12-10,
V5,Vendor E (handyman),Re-caulk tub,R4,reported done,2026-12-13,no,2026-12-13,
V6,Vendor E (handyman),Rehang closet door,R5,blocked,2026-12-15,no,2026-12-13,No access: key not at the unit
V7,Vendor B (cleaner),Window cleaning,R10,booked,2026-12-17,no,2026-12-12,
```

## The checklist

UNIT TURNOVER READINESS CHECKLIST: Quillon Yard Apartments, unit 4B

For: property manager. Prepared: Monday 14 December 2026. Move-out: Saturday 5 December 2026. Approved move-in: Saturday 19 December 2026. Needed by: Friday 18 December 2026 (4 days from today; 1 day before move-in).
Sources: move-out record (9 items); turnover checklist (10 items); vendor and work updates (7 updates); settings.
Lines: 18 (8 repairs, 10 checklist items). Reported complete: 4. Open: 14. Flagged: 8. Decisions: 9.
Readiness is for the property manager to decide after verifying the unit. This checklist does not say the unit is ready.

1. REPAIRS FROM THE MOVE-OUT RECORD
R1 Kitchen: dishwasher does not drain. Noted 5 Dec. Open: booked for 16 Dec, vendor confirmed. Update V3, Vendor C (appliance repair), repair dishwasher drain; status booked, promised Wed 16 Dec, vendor confirmed yes, updated 12 Dec.
R2 Living room: carpet stained near the window. Noted 5 Dec. Open: booked for 21 Dec, vendor confirmed. Update V4, Vendor D (flooring), replace living room carpet section; status booked, promised Mon 21 Dec, vendor confirmed yes, updated 10 Dec. FLAG, promised after needed-by, update is old: the work is promised 3 days after the needed-by date and 2 days after the move-in; the update is 4 days old. See decision 1.
R3 Bedroom: wall scuffs and nail holes. Noted 5 Dec. Reported complete: vendor confirmed. Update V1, Vendor A (painter), patch and repaint bedroom walls; status reported done, promised Fri 11 Dec, vendor confirmed yes, updated 11 Dec.
R4 Bathroom: tub caulk cracked. Noted 5 Dec. Open: reported done, completion not confirmed. Update V5, Vendor E (handyman), re-caulk tub; status reported done, promised Sun 13 Dec, vendor confirmed no, updated 13 Dec. FLAG, completion not confirmed. See decision 2.
R5 Bedroom: closet door off its track. Noted 5 Dec. Open: blocked. Update V6, Vendor E (handyman), rehang closet door; status blocked, promised Tue 15 Dec, vendor confirmed no, updated 13 Dec. Note: "No access: key not at the unit". FLAG, blocked. See decision 3.
R6 Hallway: smoke alarm chirping. Noted 5 Dec. Open: no work recorded. FLAG, no work recorded. See decision 4.
R7 Living room: blind has two bent slats. Noted 5 Dec. Open: condition unclear. FLAG, condition unclear. See decision 5.
R8 Bathroom: chip in tub enamel; former tenant says it was there at move-in. Noted 5 Dec. Open: condition record disputed, no work recorded. FLAG, no work recorded, condition record disputed. See decision 6.
No repair needed: R9 Kitchen, cabinet hinge tight but sound.

2. CLEANING
C1 Appliances cleaned inside and out. Open. Checklist status: not done, 13 Dec. No update covers it.
C2 Full turnover clean (floors, bathroom, kitchen). Open: booked for 17 Dec, not confirmed by the vendor. Update V2, Vendor B (cleaner), full turnover clean; status booked, promised Thu 17 Dec, vendor confirmed no, updated 9 Dec. FLAG, awaiting vendor confirmation, update is old: the update is 5 days old. See decision 7.

3. KEYS AND ACCESS
C3 Unit key set cut and tagged (2 sets). Reported complete. Checklist status: done, 12 Dec. No update covers it.
C4 Mailbox key and building fob programmed. Open. Checklist status: not done, 12 Dec. No update covers it.
C5 Locks rekeyed. Reported complete. Checklist status: done, 10 Dec. No update covers it.

4. UTILITIES
C6 Electricity moved to the owner's name from the move-out date. Reported complete. Checklist status: done, 8 Dec. No update covers it.
C7 Gas account moved to the owner's name from the move-out date. Open: status not supplied. FLAG, status not supplied. See decision 8.
C8 Water and trash set up for the incoming tenant. Open. Checklist status: not done, 12 Dec. No update covers it.

5. OTHER CHECKLIST ITEMS
C9 Photos of the unit taken for the file. Open. Checklist status: not done, 13 Dec. No update covers it.
C10 Property manager's walk-through of the unit. Open. Checklist status: not done, no date. No update covers it.

6. VENDOR CONFIRMATIONS STILL OUTSTANDING
V2 Vendor B (cleaner), full turnover clean, covers C2: booked date (Thu 17 Dec) not confirmed; updated 9 Dec.
V5 Vendor E (handyman), re-caulk tub, covers R4: completion (reported done Sun 13 Dec) not confirmed; updated 13 Dec.
V6 Vendor E (handyman), rehang closet door, covers R5: blocked: the visit, promised Tue 15 Dec; updated 13 Dec.
V7 Vendor B (cleaner), window cleaning, covers R10: booked date (Thu 17 Dec) not confirmed; updated 12 Dec. The item is not on the record.

7. DECISIONS FOR THE PROPERTY MANAGER: 9
1. R2, promised after needed-by, update is old. Vendor D is booked to replace the carpet section on Mon 21 Dec, vendor confirmed; the needed-by date is Fri 18 Dec and the move-in Sat 19 Dec. The last update was 10 Dec. Does Vendor D have an earlier date, or will the needed-by date or the move-in date change? Is there a newer update than 10 Dec?
2. R4, completion not confirmed. Vendor E reported the tub re-caulked on 13 Dec; the vendor has not confirmed completion. Has the vendor or the property manager confirmed the work is complete?
3. R5, blocked. The closet door visit is blocked: "No access: key not at the unit". Is the cause in the note still current, and who clears it before Fri 18 Dec?
4. R6, no work recorded. The hallway smoke alarm was noted chirping and no update covers it. Is work booked? If so, which vendor and what date?
5. R7, condition unclear. The living room blind has two bent slats; the record says a repair is unclear. Does the record need to say repair or no repair?
6. R8, no work recorded, condition record disputed. The record notes a chip in the tub enamel; the former tenant says it was there at move-in, and no work is recorded. Is work booked? If so, which vendor and what date? Which record does the property manager treat as current for this turnover? This checklist takes no side.
7. C2, awaiting vendor confirmation, update is old. Vendor B is booked for Thu 17 Dec, one day before the needed-by date; the vendor has not confirmed and the last update was 9 Dec. Has the vendor confirmed the date? If not, who asks, and by when? Is there a newer update than 9 Dec?
8. C7, status not supplied. The checklist has no status for the gas account. What is its status?
9. V7, unmatched update. Vendor B is booked for window cleaning on Thu 17 Dec, covering R10, which is not an ID in the move-out record or the checklist. Should R10 be added to the record, or does the update belong to another item?

8. THINGS TO CHECK
- R6 (move-out record, finding): the finding uses the words "smoke alarm". This checklist does not assess it. Who looks at it, and when?

9. DRAFT MESSAGE TO THE INCOMING TENANT
HOLD: not for sending until the property manager has verified the unit and approved this message.
Hello,
Your move-in at Quillon Yard Apartments, unit 4B, is Saturday 19 December 2026. Keys will be handed over on Saturday 19 December 2026 at 10:00 at the leasing office. If you have a question before then, please contact the leasing office.

Draft for the property manager. Nothing has been verified, booked, sent or changed. This checklist certifies nothing about the unit's habitability, safety or compliance with any code.
