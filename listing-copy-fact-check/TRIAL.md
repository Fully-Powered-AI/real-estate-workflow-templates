# Trial: Listing copy fact check, run on its invented example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-10

This is the second run. The first run, earlier the same day, was followed by an independent review that found the example and the template out of step: the example treated photos as viewed while only labels were given, two statements were numbered out of order, and one example sentence went beyond its photo label. The template and the example were changed to settle those points, and the template was then run again on the changed example. This second run was made by the assistant that made those changes, which therefore knew the template; the run below follows the instruction block as it now stands. The first run's record is replaced by this one. Its findings are summarised under "What the first run found".

The inputs are the invented example in `public/example.md` (Unit 4C at Fernhollow Lofts, an invented building). No client data was used.

## Inputs used

Everything under "What the person supplies" in `public/example.md`: the eight-row property sheet dated 5 November 2026, two measurement rows, four amenities, four photo labels (P1 to P4, listed only, no images), the firm's guidelines G1 to G4, the agent's draft, the channel and 90-word limit, the roles, and the run date of 12 November 2026.

## What came out

```
LISTING COPY FACT CHECK: Unit 4C, Fernhollow Lofts, 12 November 2026

For: Broker A, with Reviewer A. Run by: listing agent.
Prepared from: property sheet dated 5 November 2026 (8 rows), 2 measurement rows, 4 amenities, 4 photos (listed only), the firm's advertising guidelines (G1 to G4), the supplied draft.
Partial: the photos were listed only, not viewed, so no statement rests on one.

1. DRAFT COPY (supported statements only)
Listing description: Two-bedroom condominium unit on the 4th floor, 912 sq ft in total (measured by Measurer A, 3 November 2026), with a 252 sq ft living room (same measurement). Hardwood floors in the living room and bedrooms. In-unit washer and dryer, 1 assigned space in the garage, and bike storage on the ground floor. Shared rooftop terrace for building residents. Available 1 January 2027. $2,850 per month.
Statements in the copy: S3, S4, S6, S8, S10, S14, S16, S17, S18, S19, S20.

2. YOUR DRAFT, MARKED
Sun-drenched [S1 unsupported], luxury [S2 unsupported] 2-bedroom [S3 supported] loft [S4 corrected: the sheet says condominium unit, 4th floor] ideal for a busy couple [S5 unsupported]. 912 sq ft [S6 supported] of open living [S7 unsupported] with hardwood floors throughout [S8 corrected: living room and bedrooms only]. Steps from the subway [S9 unsupported]. In-unit laundry [S10 supported], a gym [S11 contradicted: the fitness room is Planned], concierge service [S12 unsupported] and a stunning [S13 unsupported] rooftop terrace [S14 supported]. Pet friendly [S15 unsupported]. Available now [S16 corrected: 1 January 2027] at $2,850 [S17 supported].

3. FACT CHECKLIST
S1. "Sun-drenched". Kind: description. Result: UNSUPPORTED. Source: none. Action: left out.
S2. "luxury". Kind: description. Result: UNSUPPORTED. Source: none. Action: left out.
S3. "2-bedroom". Kind: number. Result: SUPPORTED. Source: sheet row Bedrooms. Action: used.
S4. "loft". Kind: feature. Result: CORRECTED. Source: sheet row Type. Action: used as corrected: condominium unit, 4th floor.
S5. "ideal for a busy couple". Kind: audience. Result: UNSUPPORTED. Source: none. Action: left out.
S6. "912 sq ft". Kind: number. Result: SUPPORTED. Source: measurement row Total interior. Action: used, with its basis.
S7. "open living". Kind: description. Result: UNSUPPORTED. Source: none. Action: left out.
S8. "hardwood floors throughout". Kind: feature. Result: CORRECTED. Source: sheet row Flooring. Action: used as corrected: living room and bedrooms.
S9. "Steps from the subway". Kind: place. Result: UNSUPPORTED. Source: none. Action: left out.
S10. "In-unit laundry". Kind: feature. Result: SUPPORTED. Source: sheet row Laundry. Action: used.
S11. "a gym". Kind: amenity. Result: CONTRADICTED. Source: amenity row Fitness room (Planned). Action: left out.
S12. "concierge service". Kind: amenity. Result: UNSUPPORTED. Source: amenity row Concierge (Unconfirmed). Action: left out.
S13. "stunning". Kind: description. Result: UNSUPPORTED. Source: none. Action: left out.
S14. "rooftop terrace". Kind: amenity. Result: SUPPORTED. Source: amenity row Rooftop terrace (Confirmed). Action: used, with its note: shared, for building residents.
S15. "Pet friendly". Kind: feature. Result: UNSUPPORTED. Source: sheet row Pets (to be confirmed). Action: left out.
S16. "Available now". Kind: availability. Result: CORRECTED. Source: sheet row Available. Action: used as corrected: 1 January 2027.
S17. "$2,850". Kind: price. Result: SUPPORTED. Source: sheet row Rent. Action: used, as $2,850 per month.
S18. "252 sq ft living room". Kind: number. Result: SUPPORTED. Source: measurement row Living room. Action: used, with its basis (added from the measurements).
S19. "1 assigned space in the garage". Kind: feature. Result: SUPPORTED. Source: sheet row Parking. Action: used (added from the sheet).
S20. "bike storage on the ground floor". Kind: amenity. Result: SUPPORTED. Source: amenity row Bike storage (Confirmed). Action: used (added from the amenity list).

4. HELD OUT OF THE COPY, AND WHAT WOULD SETTLE IT
1. S1, S2, S7, S13: descriptive words with no source. A source for each (for example a floor plan for "open living"), or the broker accepts their absence.
2. S5: a claim about the kind of person the unit suits. The broker decides; Reviewer A sees it in section 5.
3. S9: the station's name and a distance or walking time from a source the broker accepts.
4. S11: the fitness room is Planned and under renovation with no reopening date. The broker decides whether to drop it or add it once a date exists.
5. S12: confirmation from the building that a concierge exists, and what it covers.
6. S15: the owner's pet policy, supplied in writing.

5. FOR THE DESIGNATED REVIEWER
1. S5: touches G1. A claim about who the unit suits; not in the copy.
2. S9: touches G2. A distance claim with no source; not in the copy.
3. S17: touches G3. Rent appears as $2,850 per month, the only terms on the sheet; no lease length was supplied.
4. P1 to P4: touch G4. Listed only, not viewed. No photo is used in the copy. By label, P1 to P3 show rooms of the unit; P4 shows the shared rooftop terrace, outside the unit.
This review gives no opinion on whether any item meets an advertising requirement.

6. COUNTS AND COVERAGE
Statements: 20. Supported 8. Corrected 3. Unsupported 8. Contradicted 1. In the copy: 11. Held out: 9.
Inputs used: property sheet, measurements, amenity list, photos (labels only), advertising guidelines, the supplied draft, roles, run date.
Inputs missing: none.
Could not judge: whether the property sheet itself is correct; whether any wording meets an advertising requirement; the photos (not viewed).

Draft for Broker A. Approve the facts and the copy, or change them; Reviewer A checks section 5. Nothing has been published, posted or changed in any listing record.
```

Checks: 8 + 3 + 8 + 1 = 20. In the copy 8 + 3 = 11. Held out 8 + 1 = 9. The copy is 66 words (counted by whitespace), under the 90-word limit.

## What was observed

- Every required part was produced, in the order the format gives. No stop condition applied: headers matched, all four amenity statuses were allowed, a sheet and a draft were present.
- The output is the same as the result printed in `public/example.md`. This is expected and is not independent confirmation: the example's result was rewritten from the first run's output after the fixes, and this run reproduced it from the inputs alone. The statement numbers, results, counts and the copy match; numbering follows order of appearance ("stunning" S13, then the terrace S14), and the added statements S18 to S20 follow the order they appear in the copy.
- Checked against the inputs, every statement in the copy traces to a sheet row, a measurement row or a Confirmed amenity. No fact appears in the output that is not in the inputs. No statement rests on a photo.
- Nothing was approved, published or changed by the assistant.

## What the first run found

Recorded so the changes can be followed. The first run's output is not reproduced.

- The example's photo-based statements (tall east windows, white cabinets and a stainless range) could not be reproduced from text labels, and the template said both that a label supports something and that an unviewed photo supports nothing. Settled: an unviewed photo supports nothing, and the example now lists photos by label only.
- The example numbered "stunning" and the terrace out of order. Settled: renumbered by order of appearance.
- "Loft" against a sheet reading condominium unit: the rules did not say whether this is CORRECTED or UNSUPPORTED. Settled: a different word for the kind of property is CORRECTED when a source names what it is.
- Whether adding an amenity's note ("shared") changes SUPPORTED, where added statements sit in the numbering, what "Held out" means, and what to print when no photo is used. Settled in the template.

## Open points after this run

- Compound phrases such as "In-unit laundry, a gym, concierge service" are split one claim each; the template says one claim each but gives no further guidance on lists.
- The template does not say whether a mark goes after a word or a phrase when a statement is a single adjective before a noun; the output puts it after the word.
- These changes were made before this run and were run once. Anything changed after this run has not been run again.
- After this run an independent review asked for small edits to the template: the acceptance test for an unviewed photo now matches the rule, the instruction block gained the brief-only step, "common knowledge" and the two-values exception, comma lists and mark placement are stated, the format allows a short note on "used" and a row count on the property sheet, and a test for a viewed photo was added. The example's inputs and the output printed above were not changed, and the template was not run again after these edits.
