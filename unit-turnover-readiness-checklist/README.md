# Unit turnover readiness checklist

Between one tenant and the next, the property manager gets one page for the unit: every recorded repair, the cleaning, keys, utilities and vendor confirmations still open against the approved move-in date, each gap written as a question. Nothing is sent.

*Workflow template · Real estate · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/unit-turnover-readiness-checklist/)*

## The outcome

A turnover stops depending on whoever remembers it. Every repair noted at move-out sits on one page beside what is known about it: who is booked, for which day, whether the vendor has confirmed, and how old that news is. Cleaning, keys and utilities sit beside them, each with its status as recorded.

The page works backwards from the approved move-in date. It sets a needed-by date a set number of days earlier, so the manager's own walk-through has room, and flags any work promised after it. It also names what usually surfaces the day before a move-in: a repair nobody has booked, a vendor who never confirmed, work reported done with no confirmation, a visit blocked for lack of access, a condition record the former tenant disputes. Each arrives as a question for the manager with the facts beside it.

The checklist never says the unit is ready. The property manager walks the unit and decides that. The AI assistant checks no habitability, safety or code requirement, books nothing, contacts no vendor and sends nothing, including the message to the incoming tenant, which it drafts for approval and marks to hold until the manager has verified the unit.

## Who starts the work, and when

The property manager, or whichever coordinator handles turnovers for them, begins as soon as the inspection of the vacated unit is on file and a move-in date has been agreed. After that it is worth running whenever news arrives: a vendor reports back, a date shifts, or a key or utility step is finished. A last run the day before the manager walks the unit catches what changed overnight.

The manager verifies the unit, decides when it is ready and approves any message to the incoming tenant.

## What they supply

- **The move-out record.** Each finding from the inspection: where in the unit, what was found, whether a repair is needed, whether the former tenant disputes it, and the date it was noted.
- **The turnover checklist.** Your standing list for cleaning, keys, utilities and anything else, each item with its status as of now.
- **Vendor and work updates.** Each booking or report: the vendor, the work, which finding or checklist item it covers, its status, the promised date, whether the vendor has confirmed, and the date of the update.
- **The settings.** Which property and unit, who the page is for, today's date, when the tenant moved out and the agreed move-in date, plus two limits you choose (how early the unit must be finished and how stale a vendor's news may get). If you want a tenant message drafted, add the handover day, time and place and a contact name.

Each file comes with set column headings. If a heading does not match, the work stops and asks rather than guessing.

## What comes out

One page in a fixed order. A header with the dates, the sources and the counts. Then repairs, cleaning, keys, utilities and other checklist items, each line marked reported complete or open with its basis; the vendor confirmations still outstanding; one decision for each flagged line; the things worth a second look; and, if asked for, a draft message to the incoming tenant that holds until you approve it.

A good page can be checked against the work-order list and the key log in ten minutes, and the manager recognizes every line on it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where the turnover is a repeated process that should run the same way every time.
- [Customer support and service](https://fullypowered.ai/functions/customer-support-and-service/), where the incoming tenant's first impression is set by whether the unit is ready on the day.
- [Real estate](https://fullypowered.ai/industries/real-estate/), where every vacant day costs rent and every missed item costs a complaint.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the turnover routine lives in one coordinator's head and should live on a page.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when more units and more vendors turn over than one person can follow.

## What has to change for your company

Start from your own turnover checklist; the workflow template adds no standard items of its own. Set your own two limits for finishing early and for stale vendor news; if you leave them blank the page assumes one day and three days. Choose who walks the unit, who signs off that it is ready and who may release the tenant message. Agree the status words your team uses for work and keys. Name the person who calls vendors, because the assistant never does. It runs in ChatGPT, Claude, Copilot or Gemini from files you supply, with no connection to your property system. [Preventive maintenance plan](https://fullypowered.ai/workflows/preventive-maintenance-plan/) covers the building's equipment through the year, and [project handover readiness check](https://fullypowered.ai/workflows/project-handover-readiness-check/) is the sibling for project handovers. [Supplier delivery date check](https://fullypowered.ai/workflows/supplier-delivery-date-check/) suits materials ordered for a repair.

## What has been checked

Fully Powered AI wrote this workflow template from its own published map of the work. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026, and the record is published with it; small edits made after that run have not been run again. It has not yet been tested in a client environment. It has not been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini. It certifies nothing about the condition of a unit.

Testing in your environment means running it on two or three past turnovers your coordinator remembers well, plus hard cases written in advance, each with its expected behavior: a renamed column, work promised after the needed-by date, a repair with no booking, a disputed condition record, a visit blocked for access. The manager checks every line against the work orders before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Preventive maintenance plan](https://fullypowered.ai/workflow templates/preventive-maintenance-plan/)
- [Project handover readiness check](https://fullypowered.ai/workflow templates/project-handover-readiness-check/)
- [Supplier delivery date check](https://fullypowered.ai/workflow templates/supplier-delivery-date-check/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
