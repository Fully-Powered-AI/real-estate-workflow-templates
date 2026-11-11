# Rent roll to lease abstract match

Capability template, version 0.1.0.

## Purpose

Compare a property's rent roll with its verified lease abstracts and executed amendments, unit by unit, on four fields: monthly rent, area, commencement and expiration. The output is a review document listing every difference, every item that needs a person's confirmation and every unit or field that could not be compared. The assistant reads and interprets no lease. It compares only the fields people supply, applies only amendments marked verified, and changes no record. The property accountant and the lease administrator decide which record is wrong and approve every correction.

## When to use it and when not to

Use it when a monthly rent roll is ready for review, when a property changes hands or management team, or before a rent roll goes into an owner, lender or buyer package.

Do not use it to read a lease and produce an abstract, to decide what a lease clause means, to check what tenants have paid, to value the property or to advise on any transaction. Do not use it when the abstracts have not been verified by a person: the comparison is only as good as the record it compares against.

## Roles

- **Starts it and supplies the exports:** the property accountant or the lease administrator.
- **Verifies the abstracts and marks each amendment verified or not:** the lease administrator.
- **Reviews the differences:** the other of the two.
- **Approves corrections to the rent roll:** the property accountant.
- **Approves corrections to the abstracts or the amendment register:** the lease administrator.

## Inputs

All three are exports or files that people supply. Use the default headers below, or rename your columns once to match. If a header does not match, stop and ask which of your columns is meant; never guess.

1. **Rent roll,** with an as-of date. Default headers: `Unit`, `Tenant`, `Area (sq ft)`, `Monthly Rent`, `Lease Start`, `Lease End`. If the rent column is annual rather than monthly, stop and ask.
2. **Verified lease abstracts,** one row per unit. Default headers: `Unit`, `Tenant`, `Area (sq ft)`, `Monthly Base Rent`, `Commencement Date`, `Expiration Date`, `Rent Abatement Through`, `Commencement Condition`. The last two may be blank on every row; the columns must still be present; if either header is absent, stop and ask.
3. **Amendment register.** Default headers: `Unit`, `Amendment ID`, `Effective Date`, `Field`, `New Value`, `Verified`. `Field` is one of `Monthly Base Rent`, `Area (sq ft)`, `Commencement Date`, `Expiration Date`. `Verified` is Y or N. If missing, say no amendments were supplied and compare against the abstracts alone.
4. **Charge schedules,** optional, one per unit. They are used only to answer a flagged question when a person asks; they are never used to change a comparison.
5. **Settings,** with these defaults: as-of date is the rent roll's own date; [your rent tolerance] is 0.00; [your area tolerance] is 0 sq ft; dates must match exactly.

## The procedure

1. **Check the headers and the values.** Every default header must be present in each file. Dates must be readable as one consistent format; numbers may carry currency signs and thousands separators, which are removed. If a header is missing or a value cannot be read, stop and name the file, the column and the first row.
2. **Check the units.** Match by the unit identifier, ignoring case and surrounding spaces and nothing else. If a unit appears twice on the same side, do not compare it; list it under Not compared. A unit on the roll without an abstract, or in the abstracts without a roll row, is listed under Not compared with that reason.
3. **Build the verified record for each unit.** Start with the abstract's value for each of the four fields. Then apply amendments that meet all of these: marked Y, effective on or before the as-of date, and naming a unit and field that exist. For a field with several such amendments, the one with the latest effective date wins. Two such amendments with the same effective date and different values are a conflict: do not choose; mark the field Flagged, hold that field's comparison and, if it is rent, leave the unit out of the rent totals. Amendments marked anything other than Y, effective after the as-of date, or naming an unknown unit or field are not applied; list each under Amendments not applied with its reason.
4. **Compare the four fields for each unit that is on both sides.** A blank on either side is not a match: list the field under Fields not compared with "blank on the roll" or "blank in the abstract". A field entry is not a unit: the unit is still counted in one of the groups in step 8. Otherwise compare with the tolerances. Rent difference is roll minus verified record; state whether the roll is higher or lower. Name each field by the roll's column header, even where the abstract or the amendment register names it differently (Lease End on the roll, Expiration Date in the abstract).
5. **Handle the two supplied conditions.** If Rent Abatement Through holds a date on or after the as-of date, do not compare that unit's rent; flag it with the date and compare the other fields. If Commencement Condition is not blank, compare Commencement Date as normal but flag the unit and quote the condition exactly as supplied. Never decide whether a period or condition applies.
6. **Say where each difference came from.** For every difference give the unit, tenant, field, roll value, verified value, the source of the verified value (the abstract, or the amendment ID), the size and direction (a date gap is given in days). If the roll equals the abstract's original value but not the amended value, say so. If the unit has no amendment for that field, say so. If an unverified or future-dated amendment was not applied, it is listed under Amendments not applied and is not repeated on the unit, even where the unit is Matched. End each with a question for the reviewer, never an answer.
7. **Total the rent.** For the units where rent was compared, add the roll rent and the verified rent, and show the difference. State the units left out. Also give the rent roll total as supplied and its number of units.
8. **Sort the units.** Each unit that was on both sides is counted in exactly one of: no difference or flag; differences; flagged. A unit with both a difference and a flag is counted under Differences and also listed under Flagged marked "also under Differences"; the Scope count for Flagged covers only units flagged without a difference, and the Scope line then adds "Counted under Differences and also listed under Flagged: [units]." so the arithmetic can be followed. Check that those counts plus Not compared account for every unit on either side. Field entries under Fields not compared are not units and are not counted.
9. **Return the review document** in the output format, to the person who started it. Do not send it onward.

## Exceptions and stop conditions

- **A header is missing or does not match, or a date or number cannot be read:** stop; name the file, column and row.
- **The rent roll has no as-of date:** stop and ask for it.
- **Two verified amendments conflict for the same field:** flag the field; choose neither; hold that field's comparison and, if it is rent, leave the unit out of the rent totals.
- **The abstracts or amendments appear unverified (a Verified column is absent or has no Y at all):** say so at the top.
- **Asked to correct the rent roll, edit an abstract, mark an amendment verified, interpret a clause, work out what rent should be during a free-rent period, or send the document:** decline. The property accountant and the lease administrator decide, and the assistant only prepares.
- **Asked to conclude that a difference is an error or that the tenant owes or is owed money:** decline; list the facts and the question.

## Output format

```
RENT ROLL TO LEASE ABSTRACT MATCH: [property], rent roll as of [date]

For: [property accountant] and [lease administrator], for review before any correction. Sources: rent roll ([n] units), verified lease abstracts ([n] units), amendment register ([n] entries). Tolerances: [rent], [area], dates exact.

Scope: Units compared: [n]. No difference or flag: [n]. Differences: [n]. Flagged: [n]. Not compared: [n].

Differences for review: [n].
1. Unit [unit], [tenant], [field]: roll [value]; verified record [value] ([abstract, or amendment ID, verified, effective date]); roll [higher or lower] by [size]. [Roll equals the original abstract, not the amendment. / No amendment on file.] Question: [for the reviewer].

Flagged for confirmation: [n].
1. Unit [unit], [tenant]: [abatement date or commencement condition as supplied, or amendment conflict]. [What was held or compared.] Confirm [what a person must confirm].

Not compared: [n] units.
1. Unit [unit], [tenant]: [reason: no abstract, not on the roll, or duplicate].

Fields not compared: [n]. The unit is still counted above.
1. Unit [unit], [tenant], [field]: [blank on the roll, or blank in the abstract].

Amendments not applied: [n]. [Amendment ID, unit, field, new value, effective date: reason.]

Matched: [n] units match on every field compared: [units, with the amendment ID where one was applied].

Rent totals: Rent compared for [n] units ([units left out]). Roll [amount]; verified record [amount]; roll [higher or lower] by [amount]. Rent roll total as supplied: [amount] across [n] units.

Could not assess: [anything that needs information not supplied].

Prepared for [property accountant] and [lease administrator] to review. The roll, the abstracts and the amendment register are unchanged, and nothing has been sent.
```

When a section is empty, print "None." after its heading. Never leave a section out. "Matched" is the same set of units as "No difference or flag" in the Scope line, so the two numbers are always equal. A unit with an unapplied amendment is still Matched when every field compared agrees.

## Reviewer checklist

1. The headers matched the defaults, or the mapping was confirmed. (Property accountant)
2. Every unit on either side appears exactly once in the counts. (Property accountant)
3. Every difference quotes the roll value, the verified value and its source, and the size is arithmetically right. (Lease administrator)
4. Only amendments marked verified and effective by the as-of date were applied. (Lease administrator)
5. Every flagged item quotes the abstract exactly and none has been decided. (Lease administrator)
6. The rent totals add up and name the units left out. (Property accountant)
7. No section was dropped and none states a conclusion about who is right. (Both)

## Acceptance tests

Proposed tests. Tests 1 to 5 and 7 to 9 were run once on the invented example (see the trial record published with this capability template); test 6 was not run, because the example has no amendment effective after its as-of date; tests 10 to 12 were not tried.

1. **Clean unit.** All four fields match. Expected: counted under Matched, no mention elsewhere.
2. **Rent difference, no amendment.** Roll 3,900.00, abstract 3,750.00. Expected: difference, roll higher by 150.00, "No amendment on file".
3. **Amendment never entered on the roll.** Roll shows the original expiration; a verified amendment moved it. Expected: difference with the amendment ID and "roll equals the original abstract".
4. **Amendment applied.** Roll rent equals a verified amendment's new rent. Expected: Matched, with the amendment ID.
5. **Unverified amendment.** Marked N. Expected: not applied, listed with its reason.
6. **Future-dated amendment.** Effective after the as-of date. Expected: not applied, listed with its reason.
7. **Free-rent period.** Abatement date on or after the as-of date. Expected: rent held and flagged; other fields compared.
8. **Conditional commencement.** Condition text present. Expected: flagged with the text quoted exactly.
9. **Unit on one side only.** Expected: Not compared with the reason; included in the counts.
10. **Header mismatch.** Roll column named `Rent (Annual)`. Expected: stops and asks.
11. **Conflicting amendments.** Two verified, same effective date, different values. Expected: flagged; neither chosen.
12. **Asked to fix the roll.** Expected: declines.

## Instructions for the AI assistant

```
You compare a property's rent roll with its verified lease abstracts and
executed amendments, for the property accountant and the lease
administrator. You read and interpret no lease. You compare only the fields
people supply. You never change the rent roll, an abstract or the amendment
register, never mark anything verified, and never send anything. A person
approves every correction.

The user will supply: the rent roll with its as-of date; the verified lease
abstracts; the amendment register; optionally charge schedules, which you use
only to answer a flagged question when a person asks and never to change a
comparison; and settings (tolerances default to exact). Use these default
headers. Rent roll: Unit, Tenant, Area (sq ft), Monthly Rent, Lease Start,
Lease End. Abstracts: Unit, Tenant, Area (sq ft), Monthly Base Rent,
Commencement Date, Expiration Date, Rent Abatement Through, Commencement
Condition. Amendments: Unit, Amendment ID, Effective Date, Field, New Value,
Verified. If a header does not match, a value cannot be read, the rent roll
has no as-of date, or the rent column is annual rather than monthly, stop and
ask; never guess a column.

1. Match units by identifier, ignoring case and surrounding spaces and
   nothing else. A duplicate or a unit on one side only goes under Not
   compared with the reason. A field blank on one side goes under Fields not
   compared; the unit is still counted in its group, because a field entry
   is not a unit.
2. Build the verified record per unit: the abstract's values, overridden by
   amendments marked Y, effective on or before the as-of date, for a known
   unit and field; the latest effective date wins. Two such amendments with
   the same date and different values: flag the field, choose neither, hold
   that field's comparison and, if it is rent, leave the unit out of the rent
   totals.
   List every other amendment under Amendments not applied with its reason,
   and do not repeat it on the unit. If the amendment register is absent,
   say no amendments were supplied and compare against the abstracts alone.
   If the Verified column is absent or has no Y at all, say so at the top.
3. Compare monthly rent, area, commencement and expiration within the
   tolerances. For each difference give unit, tenant, field (named by the
   roll's column header), roll value, verified value and its source, size
   and direction (a date gap in days), whether the roll equals the original
   abstract rather than the amendment, or that no amendment is on file, and
   a question for the reviewer.
4. If Rent Abatement Through is on or after the as-of date, hold the rent
   comparison and flag it. If Commencement Condition is not blank, compare
   the date and flag the unit, quoting the condition exactly. Never decide
   whether either applies.
5. Total the rent for the units where it was compared, with the units left
   out, and give the roll total as supplied.
6. Check that every unit on either side is counted exactly once: no
   difference or flag, differences, flagged (only units flagged without a
   difference), or Not compared. A unit with both a difference and a flag is
   counted under Differences and also listed under Flagged, marked "also
   under Differences", and the Scope line says so. Matched is the same set
   as No difference or flag.
7. Use the output format exactly. Print "None." for an empty section. End with
   the closing line.

Never conclude who is right, that a figure is an error, or that anyone owes
money. If asked to correct a record, interpret a clause, work out rent for a
free-rent period or send the document, decline: the property accountant and
lease administrator decide.
```

## What to customize

- Your export headers, or the mapping from them to the defaults.
- How your unit identifiers are written. Units match only on case and surrounding spaces, so "101" on the roll and "Suite 101" in the abstracts will both fall under Not compared; make the identifiers agree in the exports first.
- [your rent tolerance] and [your area tolerance], and whether any date may differ.
- What "verified" means in your amendment register and who sets it.
- Which fields beyond the four your team wants compared, such as security deposit.
- Who approves corrections to the roll and who approves corrections to the abstracts.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
- Revised after review, 10 November 2026: a date gap is given in days; a unit with both a difference and a flag is counted under Differences and also listed under Flagged; fields blank on one side have their own list and are not counted as units; the instruction block now carries every rule the procedure has. Settled from the trial: a field is named by the roll's column header; an unapplied amendment is listed only under Amendments not applied, not repeated on a Matched unit. The edits since the trial run have not been run again.
