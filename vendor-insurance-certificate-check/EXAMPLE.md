# Vendor insurance certificate check: an invented example

*Illustrative example with invented data.* The management company, the owner, the vendors, the insurers, the producers, the policy numbers, the dates and every figure below are invented. The property manager at an invented management company is checking the certificates of four service vendors across two buildings. Nothing here is a real organization's record.

## The inputs

### 1. Requirement sheet (approved by the team)

```
Approved by: regional property manager and the insurance adviser, on 2 February 2026
row,vendor_type,coverage,minimum,basis,extra_term
1,All,General liability,"$1,000,000",each occurrence,Additional insured
2,All,General liability,"$2,000,000",general aggregate,none
3,All,Workers' compensation,Present,n/a,Waiver of subrogation
4,"Landscaping, Roofing",Auto liability,"$1,000,000",combined single limit,none
5,"Elevator, Roofing",Umbrella or excess,"$5,000,000",each occurrence,none
```

### 2. Vendor roster

```
vendor,vendor_type,properties,certificate_status,contact
Vendor A Cleaning Co.,Cleaning,Buildings 1 and 2,Received 4 November 2026,Contact at Vendor A
Vendor B Grounds Inc,Landscaping,Building 1,Received 20 March 2026,Contact at Vendor B
Vendor C Lift Services,Elevator,Building 2,Received 6 July 2026,Contact at Vendor C
Vendor D Roofing,Roofing,Building 2,None received; requested 20 October 2026,Contact at Vendor D
```

### 3. Settings

```
Portfolio: Buildings 1 and 2
Requirement sheet name: Vendor insurance requirements 2026
As-of date: 16 November 2026
Date format: day, month name, year
Required certificate holder: Owner Entity X, c/o Management Company Y
Expiry window: 30 days
Endorsement copies: requested whenever additional insured is marked Yes
Reply-by date: 30 November 2026
Sign-off: Property manager, Management Company Y
```

### 4. Certificate for Vendor A

```
Insured: Vendor A Cleaning Co.
Issued: 4 November 2026 by Producer A
Certificate holder: Owner Entity X, c/o Management Company Y
Coverage 1: General liability. Insurer A. Policy GL-A-001.
  1 January 2026 to 1 January 2027. Each occurrence $1,000,000.
  General aggregate $2,000,000. Additional insured box: Yes.
Coverage 2: Workers' compensation. Insurer A. Policy WC-A-001.
  1 January 2026 to 1 January 2027. Waiver of subrogation box: Yes.
Endorsement pages supplied: none.
```

### 5. Certificate for Vendor B

```
Insured: Vendor B Grounds Inc
Issued: 17 March 2026 by Producer B
Certificate holder: Owner Entity X
Coverage 1: General liability. Insurer B. Policy GL-B-77.
  15 March 2026 to 15 March 2027. Each occurrence $500,000.
  General aggregate $1,000,000. Additional insured box: Yes.
Coverage 2: Auto liability. Insurer B. Policy AU-B-12.
  10 November 2025 to 10 November 2026. Combined single limit $1,000,000.
Endorsement pages supplied: 1 page. Form wording reads "Additional
  insured where required by written contract."
```

### 6. Certificate for Vendor C

```
Insured: Vendor C Lift Services LLC
Issued: 6 July 2026 by Producer C
Certificate holder: Owner Entity X, c/o Management Company Y
Coverage 1: General liability. Insurer C. Policy GL-C-5.
  1 July 2026 to 1 July 2027. Each occurrence $2,000,000.
  General aggregate $4,000,000. Additional insured box: Yes.
Coverage 2: Workers' compensation. Insurer C. Policy WC-C-9.
  1 July 2026 to 1 July 2027. Waiver of subrogation box: No.
Coverage 3: Umbrella. Insurer C. Policy UM-C-3.
  1 December 2025 to 10 December 2026. Each occurrence $5,000,000.
Endorsement pages supplied: 2 pages. Form wording reads "Blanket
  additional insured, ongoing operations."
```

Vendor D has no certificate.

## What the workflow template returned

**VENDOR INSURANCE CERTIFICATE CHECK: Buildings 1 and 2, as of 16 November 2026**

**1. BASIS**

Requirement sheet: Vendor insurance requirements 2026, approved by the regional property manager and the insurance adviser on 2 February 2026. Required certificate holder: Owner Entity X, c/o Management Company Y. Expiry window: 30 days. Endorsement copies: requested whenever additional insured is marked. Reply-by date: 30 November 2026.

**2. VENDORS AT A GLANCE**

- Vendor A Cleaning Co. (Cleaning): certificate received 4 November 2026; items to review 0; documents to request 1; earliest stated expiry 1 January 2027, current; draft request yes.
- Vendor B Grounds Inc (Landscaping): certificate received 20 March 2026; items to review 5; documents to request 3; earliest stated expiry 10 November 2026, expired; draft request yes.
- Vendor C Lift Services (Elevator): certificate received 6 July 2026; items to review 3; documents to request 3; earliest stated expiry 10 December 2026, expiring within the window; draft request yes.
- Vendor D Roofing (Roofing): certificate not on file; items to review not checked; documents to request 1; earliest stated expiry none; draft request yes.

**3. FIELD COMPARISON**

Vendor A Cleaning Co. (Cleaning): certificate issued 4 November 2026 by Producer A

- Insured name: Same.
- Certificate holder: Same.
- Row 1, General liability, each occurrence, minimum $1,000,000: shown $1,000,000 (Insurer A, policy GL-A-001). Limit: Meets. Term, additional insured: Shown. Dates: 1 January 2026 to 1 January 2027, current, 46 days left.
- Row 2, General liability, general aggregate, minimum $2,000,000: shown $2,000,000 (Insurer A, policy GL-A-001). Limit: Meets. Term: none required. Dates: 1 January 2026 to 1 January 2027, current, 46 days left.
- Row 3, Workers' compensation, minimum Present: shown (Insurer A, policy WC-A-001). Limit: Present. Term, waiver of subrogation: Shown. Dates: 1 January 2026 to 1 January 2027, current, 46 days left.
- Endorsements supplied: none.

Items to review: 0.

Vendor B Grounds Inc (Landscaping): certificate issued 17 March 2026 by Producer B

- Insured name: Same.
- Certificate holder: Differs. Certificate says "Owner Entity X"; required "Owner Entity X, c/o Management Company Y".
- Row 1, General liability, each occurrence, minimum $1,000,000: shown $500,000 (Insurer B, policy GL-B-77). Limit: Below by $500,000. Term, additional insured: Shown. Dates: 15 March 2026 to 15 March 2027, current, 119 days left.
- Row 2, General liability, general aggregate, minimum $2,000,000: shown $1,000,000 (Insurer B, policy GL-B-77). Limit: Below by $1,000,000. Term: none required. Dates: 15 March 2026 to 15 March 2027, current, 119 days left.
- Row 3, Workers' compensation, minimum Present: Not shown.
- Row 4, Auto liability, combined single limit, minimum $1,000,000: shown $1,000,000 (Insurer B, policy AU-B-12). Limit: Meets. Term: none required. Dates: 10 November 2025 to 10 November 2026, expired, 6 days ago.
- Endorsements supplied: 1 page, wording "Additional insured where required by written contract."

Items to review: 5. Holder differs; row 1 below; row 2 below; row 3 not shown; row 4 expired.

Vendor C Lift Services (Elevator): certificate issued 6 July 2026 by Producer C

- Insured name: Differs. Certificate says "Vendor C Lift Services LLC"; roster says "Vendor C Lift Services".
- Certificate holder: Same.
- Row 1, General liability, each occurrence, minimum $1,000,000: shown $2,000,000 (Insurer C, policy GL-C-5). Limit: Meets. Term, additional insured: Shown. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 2, General liability, general aggregate, minimum $2,000,000: shown $4,000,000 (Insurer C, policy GL-C-5). Limit: Meets. Term: none required. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 3, Workers' compensation, minimum Present: shown (Insurer C, policy WC-C-9). Limit: Present. Term, waiver of subrogation: Marked No. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 5, Umbrella or excess, each occurrence, minimum $5,000,000: shown $5,000,000 (Insurer C, policy UM-C-3, certificate says "Umbrella"). Limit: Meets. Term: none required. Dates: 1 December 2025 to 10 December 2026, expiring within the window, 24 days left.
- Endorsements supplied: 2 pages, one wording given: "Blanket additional insured, ongoing operations."

Items to review: 3. Insured name differs; row 3 waiver marked No; row 5 expiring within the window.

Vendor D Roofing (Roofing): no certificate on file. Lines that apply: rows 1, 2, 3, 4 and 5.

**4. STATED EXPIRATION DATES**

- 10 November 2026: Vendor B Grounds Inc, auto liability, policy AU-B-12: expired, 6 days ago.
- 10 December 2026: Vendor C Lift Services, umbrella, policy UM-C-3: expiring within the window, 24 days left.
- 1 January 2027: Vendor A Cleaning Co., general liability, policy GL-A-001: current, 46 days left.
- 1 January 2027: Vendor A Cleaning Co., workers' compensation, policy WC-A-001: current, 46 days left.
- 15 March 2027: Vendor B Grounds Inc, general liability, policy GL-B-77: current, 119 days left.
- 1 July 2027: Vendor C Lift Services, general liability, policy GL-C-5: current, 227 days left.
- 1 July 2027: Vendor C Lift Services, workers' compensation, policy WC-C-9: current, 227 days left.

**5. MISSING DOCUMENTS**

- Vendor A Cleaning Co.: copy of the additional insured endorsement (box marked Yes, no pages supplied, copies requested).
- Vendor B Grounds Inc: a workers' compensation certificate (not shown); a current auto liability certificate (policy AU-B-12 ended 10 November 2026); a certificate showing the required holder wording.
- Vendor C Lift Services: a certificate showing waiver of subrogation (box on WC-C-9 marked No); the renewal certificate for the umbrella (policy UM-C-3 ends 10 December 2026, 24 days left); confirmation of the vendor's name.
- Vendor D Roofing: certificates for rows 1 to 5 and an endorsement copy if additional insured is marked.

**6. QUESTIONS FOR THE INSURANCE ADVISER**

- Vendor B Grounds Inc: the endorsement page reads "Additional insured where required by written contract." Does it meet the sheet's additional insured line?
- Vendor B Grounds Inc: general liability shows $500,000 each occurrence against $1,000,000, and $1,000,000 general aggregate against $2,000,000. The sheet does not say how a vendor below its minimums is handled. How does the team want this handled?
- Vendor C Lift Services: the endorsement pages read "Blanket additional insured, ongoing operations." Does that meet the sheet's additional insured line?
- Vendor C Lift Services: the waiver of subrogation box on policy WC-C-9 is marked No against a sheet line that requires it. How does the team want this handled?
- Vendor C Lift Services: the certificate names "Vendor C Lift Services LLC"; the roster says "Vendor C Lift Services". Is this the same business?

**7. DRAFT REQUESTS (not sent)**

DRAFT, not sent. To: Contact at Vendor A. Subject: Endorsement copy for Buildings 1 and 2.

1. The certificate issued 4 November 2026 marks additional insured as Yes. Please send a copy of the additional insured endorsement.

Please reply by 30 November 2026. Property manager, Management Company Y

DRAFT, not sent. To: Contact at Vendor B. Subject: Insurance documents for Building 1.

1. Please send a workers' compensation certificate. The certificate we hold, issued 17 March 2026, does not show this cover.
2. Please send a current auto liability certificate. The policy shown, AU-B-12, ended on 10 November 2026.
3. Please send a certificate showing the holder as "Owner Entity X, c/o Management Company Y". The one we hold shows "Owner Entity X".

Please reply by 30 November 2026. Property manager, Management Company Y

DRAFT, not sent. To: Contact at Vendor C. Subject: Insurance documents for Building 2.

1. The workers' compensation entry, policy WC-C-9, has the waiver of subrogation box marked No. Our requirement sheet lists a waiver of subrogation. Please send a certificate that shows it, if one applies.
2. The umbrella policy UM-C-3 ends on 10 December 2026. Please send the renewal certificate when it is issued.
3. The certificate names "Vendor C Lift Services LLC". Please confirm the full legal name of your business.

Please reply by 30 November 2026. Property manager, Management Company Y

DRAFT, not sent. To: Contact at Vendor D. Subject: Insurance certificates for Building 2.

1. We asked for your certificates on 20 October 2026 and have none on file. Our requirement sheet lists: general liability, $1,000,000 each occurrence (additional insured) and $2,000,000 general aggregate; workers' compensation (waiver of subrogation); auto liability, $1,000,000 combined single limit; and umbrella or excess, $5,000,000 each occurrence. Please send your certificate.
2. Please show the holder as "Owner Entity X, c/o Management Company Y".
3. If additional insured is marked, please send a copy of the endorsement.

Please reply by 30 November 2026. Property manager, Management Company Y

**8. NOT CHECKED**

Policy wording; whether any endorsement does what its title suggests; whether a limit is adequate; whether a certificate is genuine or current with the producer or insurer; insurer standing; anything outside the certificates supplied. Vendor D was not checked because no certificate is on file.

**9. DECISION**

Accepted, not accepted or held, by vendor: ______ Reviewed with the insurance adviser on: ______ Signed (property manager): ______

## How the figures trace

- Days left are calendar days from 16 November 2026: to 10 December 2026 is 24; to 1 January 2027 is 46; to 15 March 2027 is 119; to 1 July 2027 is 227. 10 November 2026 is 6 days before the as-of date.
- Vendor B's shortfalls: $1,000,000 minus $500,000 is $500,000; $2,000,000 minus $1,000,000 is $1,000,000.
- Documents to request: Vendor A 1 (endorsement copy); Vendor B 3 (workers' compensation, auto liability, holder); Vendor C 3 (waiver, umbrella renewal, name); Vendor D 1 (no certificate). Vendor B's two low limits are for the adviser and are not in its draft.
- Items to review: Vendor A 0; Vendor B 5 (holder, rows 1, 2, 3 and 4); Vendor C 3 (name, row 3 waiver, row 5 dates).
