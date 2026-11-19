# Listing copy fact check

Get draft listing copy where every statement is tied to the property sheet, a measurement or a photo. The listing broker approves the copy.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Listing copy fact check on our website](https://fullypowered.ai/workflows/listing-copy-fact-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Real estate · Marketing and content · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/listing-copy-fact-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check)*

## The outcome

A listing or brochure goes to the broker with its evidence attached. Each statement in the copy points to the line of the property sheet, the measurement or the photo that backs it, so the broker is not left to remember where a number came from. Words that nothing supports, such as "sun-drenched", "steps from the subway" or an amenity nobody has confirmed, are marked and left out of the copy rather than slipped through.

Where the draft overstates a fact, the copy uses what the record supports instead: floors in some rooms are not floors "throughout", and a move-in date is the date on the sheet. The listing broker approves the facts and the copy. The designated reviewer sees every statement that touches the firm's advertising guidelines. The workflow template gives no opinion on fair housing or advertising law, and publishes nothing.

## Who starts the work, and when

The listing agent or the marketing lead runs it when a new listing or brochure is being prepared, once the property sheet, the measurements, the amenity list and the photos are in hand. It can also be run again when the broker changes a fact or the copy is revised for another channel. The broker reviews the result before the copy goes to the designated reviewer.

## What they supply

- The approved property sheet, with each fact and where it comes from.
- Verified measurements, with who measured and when.
- The amenity list, each amenity marked confirmed, planned or unconfirmed.
- The photos, attached so they can be viewed, each with a short label.
- The firm's advertising guidelines, as the reviewer's list of what to watch.
- A draft to check, or a short brief (channel, length, tone) to write from.
- The names of the listing broker and the designated reviewer.

## What comes out

One review in a fixed order. The draft copy comes first, holding only statements the record supports. Then the supplied draft with a mark after each statement, the fact checklist with one entry per statement and its source, what was held out and what would settle it, the items for the designated reviewer, and counts. Where a section is empty, it says so.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Real estate](https://fullypowered.ai/industries/real-estate/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), where brokerages, leasing teams and property marketers write listings and brochures from the property record.
- [Marketing and advertising](https://fullypowered.ai/industries/marketing-and-advertising/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), for agencies that write property copy for clients and must show where each claim comes from.
- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), which owns the copy and wants a source behind every line of it.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), when the number of listings outgrows one person's memory of each property.

It is separate from [copy edit with a change list](https://fullypowered.ai/workflows/copy-edit-with-a-change-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), which tightens existing copy, and from [store facts file](https://fullypowered.ai/workflows/store-facts-file/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check), which keeps a store's facts in one place.

## What has to change for your company

Write your own advertising guidelines as a short list the reviewer recognizes, and decide which kinds of statement always go to the designated reviewer. Decide what counts as a source (a signed property sheet, a named measurer, dated photos) and who may approve a fact. Set the channels and length limits you write for, and the words your firm never uses. Name the listing broker and the designated reviewer, and fix how a corrected fact reaches the property sheet, since the sheet stays the single record.

## What has been checked

FullyPowered AI wrote this workflow template and reviewed it editorially. It was tried on its invented example in Claude on 10 November 2026; the record is published with it. A first run was followed by an independent review the same day; the points it found were settled and the template was run again on the changed example, and the record says so. Any fix made after that second run has not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past listings whose facts your broker already knows, with cases written in advance: a feature the sheet contradicts, an amenity nobody has confirmed, a number with no measurement behind it. The broker checks every line against the record before the copy is used. The workflow template does not decide whether any wording meets an advertising requirement; your designated reviewer does.

- Written by FullyPowered AI.
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

- [Copy edit with a change list](https://fullypowered.ai/workflows/copy-edit-with-a-change-list/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check)
- [Store facts file](https://fullypowered.ai/workflows/store-facts-file/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check)
- [Obsolete copy check](https://fullypowered.ai/workflows/obsolete-copy-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=real-estate-listing-copy-fact-check&from=gh-real-estate-listing-copy-fact-check).
