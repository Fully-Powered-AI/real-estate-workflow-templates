# Vendor insurance certificate check: tried on its invented example (second run)

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (`claude-sonnet-5-5`)
- **Date:** 2026-11-10

The inputs are the invented example in [example.md](example.md) (four vendors, two buildings, one requirement sheet). No client data was used.

This is the second run. The first run, earlier on 10 November 2026, was a single attempt by a model that did not write the template; it found eleven places where the template was silent or disagreed with the example. The template, the instruction block and the example were then changed (see "What was changed after the first run"), and this record replaces the first. This second run was made by the same model that made the changes, so it is not independent of them. It was given only the instruction block and the output format from `member/template.md`, which is what the released technical file carries, and the example's inputs. It produced its own output before the example's output was compared.

## Inputs used

The "The inputs" section of [example.md](example.md): the approved requirement sheet (five rows, approved 2 February 2026, named "Vendor insurance requirements 2026"), the four-row vendor roster, the settings (portfolio "Buildings 1 and 2", as-of 16 November 2026, 30-day window, endorsement copies requested, reply-by 30 November 2026) and the certificates for Vendors A, B and C. Vendor D has no certificate.

## What came out

```
VENDOR INSURANCE CERTIFICATE CHECK: Buildings 1 and 2, as of 16 November 2026

1. BASIS
Requirement sheet: Vendor insurance requirements 2026, approved by the regional property manager and the insurance adviser on 2 February 2026. Required certificate holder: Owner Entity X, c/o Management Company Y. Expiry window: 30 days. Endorsement copies: requested whenever additional insured is marked. Reply-by date: 30 November 2026.

2. VENDORS AT A GLANCE
- Vendor A Cleaning Co. (Cleaning): certificate received 4 November 2026; items to review 0; documents to request 1; earliest stated expiry 1 January 2027, current; draft request yes.
- Vendor B Grounds Inc (Landscaping): certificate received 20 March 2026; items to review 5; documents to request 3; earliest stated expiry 10 November 2026, expired; draft request yes.
- Vendor C Lift Services (Elevator): certificate received 6 July 2026; items to review 3; documents to request 3; earliest stated expiry 10 December 2026, expiring within the window; draft request yes.
- Vendor D Roofing (Roofing): certificate not on file; items to review not checked; documents to request 1; earliest stated expiry none; draft request yes.

3. FIELD COMPARISON
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
- Certificate holder: Differs: certificate says "Owner Entity X"; required "Owner Entity X, c/o Management Company Y".
- Row 1, General liability, each occurrence, minimum $1,000,000: shown $500,000 (Insurer B, policy GL-B-77). Limit: Below by $500,000. Term, additional insured: Shown. Dates: 15 March 2026 to 15 March 2027, current, 119 days left.
- Row 2, General liability, general aggregate, minimum $2,000,000: shown $1,000,000 (Insurer B, policy GL-B-77). Limit: Below by $1,000,000. Term: none required. Dates: 15 March 2026 to 15 March 2027, current, 119 days left.
- Row 3, Workers' compensation, minimum Present: Not shown.
- Row 4, Auto liability, combined single limit, minimum $1,000,000: shown $1,000,000 (Insurer B, policy AU-B-12). Limit: Meets. Term: none required. Dates: 10 November 2025 to 10 November 2026, expired, 6 days ago.
- Endorsements supplied: 1 page: "Additional insured where required by written contract."
Items to review: 5. Holder differs; row 1 below; row 2 below; row 3 not shown; row 4 expired.

Vendor C Lift Services (Elevator): certificate issued 6 July 2026 by Producer C
- Insured name: Differs: certificate says "Vendor C Lift Services LLC"; roster says "Vendor C Lift Services".
- Certificate holder: Same.
- Row 1, General liability, each occurrence, minimum $1,000,000: shown $2,000,000 (Insurer C, policy GL-C-5). Limit: Meets. Term, additional insured: Shown. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 2, General liability, general aggregate, minimum $2,000,000: shown $4,000,000 (Insurer C, policy GL-C-5). Limit: Meets. Term: none required. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 3, Workers' compensation, minimum Present: shown (Insurer C, policy WC-C-9). Limit: Present. Term, waiver of subrogation: Marked No. Dates: 1 July 2026 to 1 July 2027, current, 227 days left.
- Row 5, Umbrella or excess, each occurrence, minimum $5,000,000: shown $5,000,000 (Insurer C, policy UM-C-3, certificate says "Umbrella"). Limit: Meets. Term: none required. Dates: 1 December 2025 to 10 December 2026, expiring within the window, 24 days left.
- Endorsements supplied: 2 pages, one wording given: "Blanket additional insured, ongoing operations."
Items to review: 3. Insured name differs; waiver of subrogation marked No; umbrella expiring within the window.

Vendor D Roofing (Roofing): no certificate on file. Lines that apply: rows 1, 2, 3, 4 and 5.

4. STATED EXPIRATION DATES
- 10 November 2026: Vendor B Grounds Inc, Auto liability, policy AU-B-12: expired, 6 days ago.
- 10 December 2026: Vendor C Lift Services, Umbrella, policy UM-C-3: expiring within the window, 24 days left.
- 1 January 2027: Vendor A Cleaning Co., General liability, policy GL-A-001: current, 46 days left.
- 1 January 2027: Vendor A Cleaning Co., Workers' compensation, policy WC-A-001: current, 46 days left.
- 15 March 2027: Vendor B Grounds Inc, General liability, policy GL-B-77: current, 119 days left.
- 1 July 2027: Vendor C Lift Services, General liability, policy GL-C-5: current, 227 days left.
- 1 July 2027: Vendor C Lift Services, Workers' compensation, policy WC-C-9: current, 227 days left.

5. MISSING DOCUMENTS
- Vendor A Cleaning Co.: endorsement copy for additional insured (box marked Yes, no pages supplied, copies requested).
- Vendor B Grounds Inc: a workers' compensation certificate (row 3 not shown); a current auto liability certificate (AU-B-12 ended 10 November 2026); a corrected certificate or confirmation of the holder wording.
- Vendor C Lift Services: a corrected certificate or confirmation of the insured name; a certificate or confirmation on the waiver of subrogation box marked No on WC-C-9; the renewal certificate for the umbrella (UM-C-3 ends 10 December 2026, 24 days left).
- Vendor D Roofing: no certificate on file (rows 1, 2, 3, 4 and 5 apply).

6. QUESTIONS FOR THE INSURANCE ADVISER
- Vendor B Grounds Inc: the endorsement page reads "Additional insured where required by written contract." Does this meet the sheet's additional insured line?
- Vendor B Grounds Inc: general liability shows $500,000 each occurrence against a $1,000,000 minimum (below by $500,000) and $1,000,000 general aggregate against $2,000,000 (below by $1,000,000). The sheet does not say how such a vendor is handled. How should it be handled?
- Vendor C Lift Services: the endorsement pages read "Blanket additional insured, ongoing operations." Does this meet the sheet's additional insured line?
- Vendor C Lift Services: the waiver of subrogation box on WC-C-9 is marked No against a sheet line that requires the term. How should it be handled?
- Vendor C Lift Services: the certificate names "Vendor C Lift Services LLC"; the roster says "Vendor C Lift Services". Is this the same business?

7. DRAFT REQUESTS (not sent)
DRAFT, not sent.
To: Contact at Vendor A
Subject: Endorsement copy, Buildings 1 and 2
1. Your certificate issued 4 November 2026 marks additional insured as Yes for policy GL-A-001, and no endorsement page came with it. Please send a copy of the endorsement.
Please reply by 30 November 2026.
Property manager, Management Company Y

DRAFT, not sent.
To: Contact at Vendor B
Subject: Insurance documents, Building 1
1. Our requirement sheet lists workers' compensation. The certificate we hold, issued 17 March 2026, does not show it. Please send a certificate that shows it.
2. The auto liability policy AU-B-12 on the certificate we hold ended on 10 November 2026. Please send a current certificate.
3. Our requirement sheet lists the certificate holder as "Owner Entity X, c/o Management Company Y". The certificate we hold shows "Owner Entity X". Please send a certificate showing the listed wording, or confirm the holder.
Please reply by 30 November 2026.
Property manager, Management Company Y

DRAFT, not sent.
To: Contact at Vendor C
Subject: Insurance documents, Building 2
1. The certificate shows the insured as "Vendor C Lift Services LLC"; our records show "Vendor C Lift Services". Please confirm the name, or send a corrected certificate.
2. Our requirement sheet lists a waiver of subrogation for workers' compensation. The waiver of subrogation box on policy WC-C-9 is marked No. Please send a certificate that shows it, or confirm the position.
3. The umbrella policy UM-C-3 shows an expiry of 10 December 2026. Please send the renewal certificate.
Please reply by 30 November 2026.
Property manager, Management Company Y

DRAFT, not sent.
To: Contact at Vendor D
Subject: Insurance certificate, Building 2
1. We asked for your certificates on 20 October 2026 and have none on file. Our requirement sheet lists: general liability, $1,000,000 each occurrence (additional insured) and $2,000,000 general aggregate; workers' compensation (waiver of subrogation); auto liability, $1,000,000 combined single limit; and umbrella or excess, $5,000,000 each occurrence. Please send your certificate.
2. Please show the certificate holder as "Owner Entity X, c/o Management Company Y".
3. If additional insured is marked, please send a copy of the endorsement.
Please reply by 30 November 2026.
Property manager, Management Company Y

8. NOT CHECKED
Policy wording; whether any endorsement does what its title suggests; whether a limit is adequate; whether a certificate is genuine or current with the producer or insurer; insurer standing; anything outside the certificates supplied. Vendor D was not checked: no certificate on file.

9. DECISION
Accepted, not accepted or held, by vendor: ______
Reviewed with the insurance adviser on: ______
Signed (property manager): ______
```

## What was observed

Every required part was produced. Nothing in the inputs triggered a stop: the headers matched, the sheet had an approver and a date, the as-of date was set, and no date could be read two ways. No password, link or instruction appeared in the certificates. The run was not asked to decline anything, so the decline rules were not exercised.

Compared with the published example, the figures, results, item counts (0, 5, 3, not checked), documents-to-request counts (1, 3, 3, 1), day counts (46, 119, 227, 24, 6 ago), the order of the seven expiry lines and the four drafts agree in substance. The differences were wording only (no figure, date, count or result differed):

- The example's adviser questions say "How does the team want this handled?"; this run said "How should it be handled?". Both stay as questions and neither recommends anything.
- The example's missing-documents lines for Vendors B and C are phrased as requests; this run phrased them as the document or confirmation needed.
- The example's Vendor A missing-documents line reads "copy of the additional insured endorsement"; this run wrote "endorsement copy for additional insured".
- The example's Vendor D missing-documents line reads "certificates for rows 1 to 5 and an endorsement copy if additional insured is marked"; this run wrote "no certificate on file (rows 1, 2, 3, 4 and 5 apply)".
- In section 4 the example writes coverage names in lower case ("auto liability", "umbrella"); this run capitalised them ("Auto liability", "Umbrella").
- The example's Vendor C waiver line in its draft says "if one applies"; this run said "or confirm the position".

No fact in this run's output is missing from the inputs.

Not settled by this run, and recorded as known gaps in the template's version notes:

1. A vendor whose only gap is a Below or Not comparable limit gets no draft request, because a low limit goes to the adviser only. That is the rule now, but a manager may expect a request in that case.
2. Names that differ in wording but not by one allowed pattern (for example "Excess liability" against "Umbrella") are Not comparable; the run did not meet that case, so the rule is untried.
3. The vendor-type-not-on-the-sheet rule was not exercised.
4. The roster's received date is used in the glance line even where it differs from the certificate's issue date (Vendor B: 20 March against 17 March 2026); the issue date is in the field comparison.

The run depends on the person supplying the facts correctly: it cannot tell whether the certificate text is genuine, and says so under Not checked.

## What was changed after the first run

The first run found these; each was settled in the template, the instruction block and the example, or recorded above as a known gap.

- The instruction block now carries every rule it needs (counting, what goes under Missing documents, the endorsement copy, what goes to the adviser, the insured-name rule, the no-shared-word stop, the vendor type the sheet does not cover, the meaning of Current).
- The example no longer adds a fourth line to Vendor B's draft: a draft lists only what is missing, and a low limit goes to the adviser.
- The glance line has a documents-to-request count, so Vendor A reads as 0 items to review and 1 document to request. The "(endorsement copy)" note is gone from the example.
- Expiry lines are one per coverage, in roster order and then sheet row order for equal dates.
- The sheet name and portfolio name are now settings, and "not named" prints where they are absent.
- Rules were added for close coverage names, a basis of n/a, endorsement page counts, the roster's received date, the holder wording in a request to a vendor with no certificate, and what a request may ask for.
- A coverage ending on the as-of date is Expiring within the window with 0 days left; the first version called it Current, which conflicted with its own definition.
