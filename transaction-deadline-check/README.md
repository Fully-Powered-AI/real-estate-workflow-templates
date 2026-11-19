# Transaction deadline check

One Monday page from your open-transactions export: milestones due soon by agent, dates passed with no completion, impossible dates and questions.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Transaction deadline check on our website](https://fullypowered.ai/workflows/transaction-deadline-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the sample ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Real estate · Operations and process improvement · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/transaction-deadline-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check)*

## The outcome

No milestone slips past quietly. Each week the transaction coordinator or managing broker sees every open deal on one page: the deposits, inspection periods, financing and appraisal dates, title work and closings coming up in the brokerage's window, sorted by agent, and every milestone whose recorded date has gone by with nothing marked complete.

The records that would cause trouble later surface now: a financing date nobody entered, a closing dated before the offer was accepted, a completion stamped with a date that has not happened yet, a deal with no agent on it. If last week's export is supplied, the page also shows what moved since then: new deals, deals that dropped off, dates that changed and completions recorded. Each problem arrives as a plain question for the agent who can answer it.

A count at the top proves the page is complete: every open transaction and every tracked milestone is accounted for, so the coordinator knows nothing was skipped.

The contract and the managing broker govern every deadline. The workflow template reads each date exactly as your system holds it. It never works out a deadline from a contract, a law or a rule about weekends and holidays, and it gives no legal advice. It contacts nobody, extends nothing and changes no record.

## Who starts the work, and when

The transaction coordinator starts it every Monday morning, before the week's calls, and again on any day a contract is amended and the new dates are in the system. Where a brokerage has no coordinator, the managing broker runs it. The coordinator decides which questions go to which agent and how; the agents answer and update the record; the managing broker decides on any deadline that is in doubt, with the contract in hand.

## What they supply

- **The open-transactions export from your real estate CRM or transaction system**, one row per open deal, with these columns: transaction ID, property, side, agent, acceptance date, and for each milestone you track (deposit due, inspection period end, financing date, appraisal, title, closing) its date as recorded with the completed date beside it. If your headers differ from the defaults, the workflow template stops and asks which column is which.
- **Today's date.**
- **Your brokerage's settings:** which milestones you track, and how many days ahead counts as due soon (seven unless you change it).
- **Last week's export,** if you want the changes since then.

Leave buyers' and tenants' personal finances, and anything touching fair-housing protected characteristics, out of the export. A deadline check needs none of it, and the workflow template stops if it finds any.

## What comes out

One page in a fixed order: the count that proves every transaction and milestone was read; milestones due in the window, by agent; milestones past their recorded date with no completion recorded, oldest first; missing or impossible dates; changes since last week's export; and the questions for each agent. A section with nothing in it says "None." The page closes by saying that every date is as recorded and that nothing was sent, extended or changed.

See the worked example in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Real estate](https://fullypowered.ai/industries/real-estate/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), where a brokerage carries dozens of open deals, each with its own inspection, financing and closing dates, and one missed date can cost a client the deal.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), where an acquisitions team tracks the milestones on its own property purchases and wants the same weekly view of what is due.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), which owns the weekly routine that keeps every open file on track.
- [Sales](https://fullypowered.ai/functions/sales/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), where agents carry their deals to closing and need to see what is theirs this week.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), when the brokerage has more open deals than one coordinator can hold in their head.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), where the Monday review lives in one long-serving coordinator's spreadsheet and should be the same every week.

It sits beside [unit turnover readiness checklist](https://fullypowered.ai/workflows/unit-turnover-readiness-checklist/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), which gets a rental unit ready between tenants, and [obligation and filing calendar review](https://fullypowered.ai/workflows/obligation-and-filing-calendar-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), which does the same kind of recorded-date check for a company's own filings and renewals, and [supplier delivery date check](https://fullypowered.ai/workflows/supplier-delivery-date-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check), which compares the promised and revised dates on open purchase orders.

## What has to change for your company

Match the column headers to your export, or rename the columns once. List the milestones you track, in the order you think about them, separately for residential and commercial deals if they differ. Set your due-soon window. Decide how your system marks a milestone that does not apply, such as financing on a cash purchase. Agree who reads the page, who sends the questions to agents and how quickly agents answer. It runs in ChatGPT, Claude, Copilot or Gemini, from the files you supply; it needs no connection to your transaction system.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 19 November 2026. It was tried on its example on 19 November 2026 in one run, published with it. Edits after that run, to the example's questions and to some format notes, have not been run again. It has not yet been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past Mondays your coordinator remembers well, with hard cases written in advance: a closing dated before acceptance, a blank financing date on a deal that has one, a cash purchase marked not applicable, a date changed by an amendment. The coordinator checks every line against the system before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check) sets those cases up.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 19 November 2026.
- Package format checked by script on every release.
- Tried once on its example in Claude on 19 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example.
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

- [Unit turnover readiness checklist](../unit-turnover-readiness-checklist/)
- [Obligation and filing calendar review](https://fullypowered.ai/workflows/obligation-and-filing-calendar-review/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check)
- [Supplier delivery date check](https://fullypowered.ai/workflows/supplier-delivery-date-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-transaction-deadline-check&from=gh-transaction-deadline-check).
