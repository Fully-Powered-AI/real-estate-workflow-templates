# Rent roll to lease abstract match

Your property accountant gets the rent roll checked against the verified lease abstracts and amendments, unit by unit: rent, area, commencement and expiration, with every difference listed for review. It compares supplied fields only and corrects nothing.

*Capability template · Real estate · Finance and accounting · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/rent-roll-to-lease-abstract-match/)*

## The outcome

The rent roll stops being something everyone assumes is right. Each month, or at a property handoff, the property accountant and the lease administrator get one list: the units that agree with the verified paperwork, the units that do not, and the units where the answer depends on something a person has to confirm.

Every difference states what the roll says, what the verified record says, where that record came from and how large the gap is. Where the roll still shows the original abstract after a verified amendment changed it, the list says so, because that points to a roll that was never updated.

The people stay in charge. The two of them decide which record is wrong, and no correction is made without their sign-off. The AI assistant changes neither the roll nor the abstracts.

## Who starts the work, and when

The property accountant or the lease administrator starts it when a monthly rent roll is ready for review, or when a property is handed over from one team or owner to another. The other of the two reviews the result before any correction is made.

## What they supply

- The rent roll export for the property, with its as-of date.
- The verified lease abstracts, one row per unit.
- The register of executed amendments, each marked verified or not, with its effective date.
- Optionally, the charge schedules, to settle which rent figure belongs in a flagged case.
- The tolerances the team accepts, if any. The default is an exact match.

## What comes out

One review document in a fixed order: the scope, the differences for review, the items flagged for confirmation, the units and fields that could not be compared, the amendments that were not applied, the units that match, a rent total that ties the compared units on both sides, and what could not be assessed from the information supplied. Empty sections say "None."

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Real estate](https://fullypowered.ai/industries/real-estate/), where the rent roll feeds owner reports, lender packages and every valuation discussion.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where an asset manager or lender receives a rent roll and wants it tied to the lease file.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the rent roll as an accounting record.
- [Acquisitions & integration](https://fullypowered.ai/situations/acquisitions-and-integration/), when a property changes hands and the incoming team needs to know the roll can be trusted.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where many properties report on a fixed rhythm and a bad roll is costly.

It is a different piece of work from [receivables exception review](https://fullypowered.ai/capabilities/receivables-exception-review/), which examines what tenants have paid, and from [weekly receivables summary](https://fullypowered.ai/capabilities/weekly-receivables-summary/), which reports on money owed. This one checks the recorded terms behind the rent, before any money is considered.

## What has to change for your company

Match the column headers to your rent roll and abstract exports, or rename the columns once. Decide your tolerances for rent and area. Name who verifies an amendment and what "verified" means in your register. Decide who signs off a change to the roll and who signs off a change to the abstracts. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your property system.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in one run in Claude; the record is published with it. The ambiguities that run found are settled in the template or listed there as open, and the small edits made afterward have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month your lease administrator already knows, with cases written in advance: a unit missing from one side, an amendment the roll never picked up, a free-rent period. The property accountant checks every difference against the lease file before anyone relies on the list.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Receivables exception review](https://fullypowered.ai/capabilities/receivables-exception-review/)
- [Bank reconciliation preparation](https://fullypowered.ai/capabilities/bank-reconciliation-preparation/)
- [Month-end close checklist](https://fullypowered.ai/capabilities/month-end-close-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
