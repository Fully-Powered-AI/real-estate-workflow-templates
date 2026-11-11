# Property diligence index

The transaction lead gets a diligence room in order: every document indexed by workstream, every checklist item and request tracked, and every open finding tied to the report or request that raised it. Specialists judge the findings; nothing is valued or sent.

*Capability template · Real estate · Project and delivery · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/property-diligence-index/)*

## The outcome

During a property transaction, reports arrive from inspectors, the title company, environmental consultants and the seller, each on its own day and in its own format. Questions come out of them faster than anyone can keep track of. This capability turns the pile into one index you can work from.

You get a document index and an open-item tracker, grouped by workstream. Each document shows its author, its dates, whether every page arrived and which checklist item and request it answers. Each checklist item shows whether it is received, received but worth a second look, requested and outstanding, or not yet requested. Each open item names the report and page, or the request, that raised it, who has it and when it is due. A count at the top proves the checklist adds up.

The index uses only what you supply. It does not read the reports, value anything or say what a finding means. Missing pages, two versions of one report and statements that conflict are listed as questions for a person.

## Who starts the work, and when

A transaction coordinator or acquisitions lead starts it when the diligence period opens, and runs it again whenever reports, answers or new items arrive. The transaction lead reviews each run, assigns the follow-up and decides what goes to which specialist.

## What they supply

- The diligence checklist, by workstream, with the date each item is due.
- The request log: what was asked of whom and when, and whether it has been answered.
- The list of documents received, with dates and page counts.
- The items raised from those documents and requests, in your words, with the page they came from.
- The agreed deal timetable, as the date the diligence period ends, plus the roles involved.

## What comes out

One index in a fixed order. At the top, a count that ties the checklist together and shows how many requests and items are open. Then each workstream in turn: its documents with flags, its checklist, its requests and its open items. After the workstreams come the conflicting statements, the items that trace to no source, and a short list of decisions for the transaction lead. Anything that cannot be matched is printed as a question, never guessed.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Real estate](https://fullypowered.ai/industries/real-estate/), where a purchase, financing or disposition rests on a stack of third-party reports.
- [Construction](https://fullypowered.ai/industries/construction/), for site acquisitions and development land with the same inspection and survey trail.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), for lenders and investors who need to see which items are still open before they rely on a package.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), which owns the timetable and the follow-up.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the same index shape serves any repeated review of outside documents.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), when a team runs several acquisitions at once.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when deal volume outgrows the folders and spreadsheets in use.

It is not an evidence index for an audit; that is [audit evidence index](https://fullypowered.ai/capabilities/audit-evidence-index/). It does not compare bids; that is [vendor quote comparison](https://fullypowered.ai/capabilities/vendor-quote-comparison/). It is not a document index for a construction lender's draw package; that is [lender draw package index](https://fullypowered.ai/capabilities/lender-draw-package-index/). It does not track the documents a client owes an engagement; that is [client document request tracker](https://fullypowered.ai/capabilities/client-document-request-tracker/). Decisions that come out of the findings can be recorded with the [decision log](https://fullypowered.ai/capabilities/decision-log/).

## What has to change for your company

Name your workstreams and keep the spelling identical in every list. Set how many days a request may sit before it is due for a chase, and how far ahead an item counts as due soon. Decide who is the transaction lead and who may assign follow-up. Agree which specialist judges which kind of finding, so the assignment is quick. Fix the column names in your exports once, so each deal starts from the same four lists.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in Claude, in one run; the record is published with it. It has not yet been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a closed deal your team already knows, with cases written in advance: a report with missing pages, two versions of one statement, a request marked received with no document, an item with no owner. The transaction lead checks every line against the lists before anyone relies on the index. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

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

- [Audit evidence index](https://fullypowered.ai/capabilities/audit-evidence-index/)
- [Vendor quote comparison](https://fullypowered.ai/capabilities/vendor-quote-comparison/)
- [Decision log](https://fullypowered.ai/capabilities/decision-log/)
- [Lender draw package index](https://fullypowered.ai/capabilities/lender-draw-package-index/)
- [Client document request tracker](https://fullypowered.ai/capabilities/client-document-request-tracker/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
