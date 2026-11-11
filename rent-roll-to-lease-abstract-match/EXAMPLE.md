# Rent roll to lease abstract match: an invented example

*Illustrative example with invented data.* One monthly review at Property X, an invented eight-tenant office building. Every tenant and amendment below is invented.

## What the person supplies

**Rent roll as of 1 November 2026** (columns: Unit, Tenant, Area (sq ft), Monthly Rent, Lease Start, Lease End)

- 101, Tenant A, 1,200, 3,000.00, 2024-03-01, 2027-02-28
- 102, Tenant B, 950, 2,375.00, 2023-07-01, 2026-06-30
- 103, Tenant C, 1,500, 3,900.00, 2025-01-01, 2028-12-31
- 104, Tenant D, 800, 2,000.00, 2025-09-01, 2030-08-31
- 105, Tenant E, 1,100, 2,750.00, 2026-10-01, 2031-09-30
- 106, Tenant F, 1,000, 2,600.00, 2022-05-01, 2027-04-30
- 107, Tenant G, 700, 1,750.00, 2024-11-01, 2027-10-31
- 108, Tenant H, 900, 2,250.00, 2026-11-15, 2029-11-14
- 110, Tenant J, 600, 1,500.00, 2026-02-01, 2029-01-31

**Verified lease abstracts** (columns: Unit, Tenant, Area (sq ft), Monthly Base Rent, Commencement Date, Expiration Date, Rent Abatement Through, Commencement Condition)

- 101, Tenant A, 1,200, 3,000.00, 2024-03-01, 2027-02-28, blank, blank
- 102, Tenant B, 950, 2,375.00, 2023-07-01, 2026-06-30, blank, blank
- 103, Tenant C, 1,500, 3,750.00, 2025-01-01, 2028-12-31, blank, blank
- 104, Tenant D, 840, 2,000.00, 2025-09-01, 2030-08-31, blank, blank
- 105, Tenant E, 1,100, 2,750.00, 2026-10-01, 2031-09-30, 2026-12-31, blank
- 106, Tenant F, 1,000, 2,500.00, 2022-05-01, 2027-04-30, blank, blank
- 107, Tenant G, 700, 1,750.00, 2024-11-01, 2027-10-31, blank, blank
- 108, Tenant H, 900, 2,250.00, 2026-11-15, 2029-11-14, blank, "Fit-out sign-off by Tenant H"
- 109, Tenant K, 650, 1,625.00, 2025-06-01, 2028-05-31, blank, blank

**Amendment register** (columns: Unit, Amendment ID, Effective Date, Field, New Value, Verified)

- 102, AM-102-1, 2026-05-01, Expiration Date, 2028-06-30, Y
- 106, AM-106-1, 2026-07-01, Monthly Base Rent, 2,600.00, Y
- 107, AM-107-1, 2026-09-01, Monthly Base Rent, 1,850.00, N

Settings: exact match on rent, area and dates; as-of date 2026-11-01.

## What comes out

**RENT ROLL TO LEASE ABSTRACT MATCH: Property X, rent roll as of 2026-11-01**

- **For:** Property accountant and lease administrator, for review before any correction. Sources: rent roll (9 units), verified lease abstracts (9 units), amendment register (3 entries). Tolerances: rent 0.00, area 0 sq ft, dates exact.
- **Scope:** Units compared: 8. No difference or flag: 3. Differences: 3. Flagged: 2. Not compared: 2.
- **Differences for review:** 3.
  1. Unit 102, Tenant B, Lease End: roll 2026-06-30; verified record 2028-06-30 (AM-102-1, verified, effective 2026-05-01); roll earlier by 731 days. The roll equals the original abstract, not the amendment. Question: was AM-102-1 entered on the roll?
  2. Unit 103, Tenant C, Monthly Rent: roll 3,900.00; verified record 3,750.00 (abstract); roll higher by 150.00. No amendment on file for this unit. Question: which record is wrong, or is an amendment missing?
  3. Unit 104, Tenant D, Area: roll 800 sq ft; verified record 840 sq ft (abstract); roll lower by 40 sq ft. No amendment on file. Question: which record is wrong?
- **Flagged for confirmation:** 2.
  1. Unit 105, Tenant E: abstract shows rent abatement through 2026-12-31, on or after the as-of date. Rent comparison held. Area, Lease Start and Lease End match. Confirm which rent figure the roll should show during the period.
  2. Unit 108, Tenant H: abstract shows a commencement condition, "Fit-out sign-off by Tenant H". Lease Start matches (2026-11-15), as do area, rent and Lease End. Confirm whether the condition has been met.
- **Not compared:** 2 units.
  1. Unit 109, Tenant K: in the abstracts, not on the rent roll.
  2. Unit 110, Tenant J: on the rent roll, no abstract supplied.
- **Fields not compared:** None.
- **Amendments not applied:** 1. AM-107-1, Unit 107, Monthly Base Rent 1,850.00, effective 2026-09-01: not verified.
- **Matched:** 3 units match on every field compared: 101, 106 (rent matches AM-106-1, verified), 107.
- **Rent totals:** Rent compared for 7 units (105 held). Roll 17,875.00; verified record 17,725.00; roll higher by 150.00, all from Unit 103. Rent roll total as supplied: 22,125.00 across 9 units.
- **Could not assess:** Whether the commencement condition for Unit 108 has been met. Charge schedules were not supplied, so no flagged question was checked against them.

Prepared for the property accountant and lease administrator to review. The roll, the abstracts and the amendment register are unchanged, and nothing has been sent.
