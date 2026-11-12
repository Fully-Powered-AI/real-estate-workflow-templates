# Property owner report

A property manager gets the month's owner report drafted from the statements and logs they supply: occupancy, collections, open maintenance and the decisions the owner is asked to make, each statement traced to its source and each gap shown.

*Workflow template · Real estate · Customer success and account management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/property-owner-report/)*

## The outcome

The owner report stops being the thing written in a rush on the fifth of the month. Once the month's statements and logs are in, the property manager has a draft that says how full the building is, what was collected and what is still owed, which repairs are open and how long they have been open, and what the owner is being asked to decide.

Every statement in the draft carries a tag naming where it came from: the operating statement, the leasing tracker, the collections report, the work-order summary or a numbered manager note. What the records cannot support is not written as fact. It sits in a short list of gaps and unconfirmed items: a work-order summary that is out of date, a tenant change nobody has signed, a rent figure that differs between two documents, a forecast with nothing behind it.

The property manager and the accountant verify the draft before the owner sees it. The AI assistant values nothing, advises on no leasing, purchase or sale decision, changes no record and sends nothing.

## Who starts the work, and when

The property manager starts it once the month's statements are in, usually in the first week after the month ends. The accountant who prepared the statements checks the collections and statement figures, and the property manager checks everything else, before anything goes to the owner. It can be run again if a late statement arrives or a correction is made.

## What they supply

- The month's operating statement, with the prior month and the budget beside it.
- The leasing tracker as of the period end: each unit, its status, its dates and its area.
- The collections report: what was charged, what was received and what is owed, by unit.
- The work-order summary, with its as-of date.
- The manager's numbered notes, including any decision the owner is being asked to make.
- Last month's report, so that open decisions carry forward.
- A few settings: the period end, how old the work-order summary may be, and what counts as a long-open repair.

## What comes out

One draft in a fixed order: a summary, then occupancy, collections, open maintenance, decisions requested, and gaps and unconfirmed items. Empty sections say "None." Each section ends in lines the property manager and accountant can check against the source. The draft closes with a verification line for both of them.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Real estate](https://fullypowered.ai/industries/real-estate/), where the building's owner expects the same account of the property every month.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where an asset manager or fund receives reports from several managers and needs them in one shape.
- [Customer success and account management](https://fullypowered.ai/functions/customer-success-and-account-management/), which owns the recurring report that goes to the owner, the client, under a manager's name.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which stands behind the collections and statement figures.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where owners compare properties on a fixed rhythm.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where a long-serving manager keeps the owner relationship in their head and the report should live on a page.

It is a different piece of work from the [weekly owner business brief](https://fullypowered.ai/workflows/weekly-owner-business-brief/), which gives a business owner one page of cash, sales and pipeline each Monday, and from [client status update preparation](https://fullypowered.ai/workflows/client-status-update-preparation/), which reports on a project's progress and a client's open decisions. This one reports on a building, from its own statements and logs, to the person who owns it. For checking the rent roll against the lease record first, see [rent roll to lease abstract match](https://fullypowered.ai/workflows/rent-roll-to-lease-abstract-match/).

## What has to change for your company

Use your own report's order if the owner already expects one, and keep it fixed. Set how old a work-order summary may be before it counts as stale, how many days make a repair long-open, and how far ahead lease endings are listed. Decide who may submit decisions for the owner and how the manager's notes are labelled. Match the column headers to your exports, or tell the assistant the mapping once. Agree who verifies which figures: the accountant for collections and statement lines, the property manager for the rest. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your property system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026; the record is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month the property manager and accountant already know, plus cases written in advance with their expected behavior: a stale work-order summary, a rent total that differs between the statement and the collections report, a lease that ended with no renewal on file, a decision carried from last month. They check every figure against the source before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Rent roll to lease abstract match](../rent-roll-to-lease-abstract-match/)
- [Weekly owner business brief](https://fullypowered.ai/workflow templates/weekly-owner-business-brief/)
- [Client-status update preparation](https://fullypowered.ai/workflow templates/client-status-update-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
