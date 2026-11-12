# Vendor insurance certificate check

For a property manager collecting insurance certificates from service vendors: each certificate's fields set beside the requirements the team already approved, every stated expiration date listed, and draft requests for what is missing. The manager reviews gaps with the insurance adviser before accepting anything.

*Workflow template · Real estate · Procurement and suppliers · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/vendor-insurance-certificate-check/)*

## The outcome

A certificate arrives in an inbox, and someone has to find out whether it says what the team asked for. This workflow template does that reading the same way every time. For each vendor it sets the certificate's fields beside your approved requirement sheet, line by line: the insured name, the certificate holder, each limit, each extra term the sheet asks for, and the dates. Where a field matches, it says so. Where it differs or is missing, it says exactly what the certificate shows and what the sheet lists. It covers vendors only; tenant certificates are out of scope.

You also get one list of every expiration date the certificates state, soonest first, so a lapse is seen weeks ahead rather than when something goes wrong in a building. Every vendor with a missing document has a draft request ready for the manager to read, edit and send.

The assistant judges nothing about coverage. It does not say whether a limit is enough, whether an endorsement works or whether a vendor should be accepted. It quotes endorsement wording and passes it to the insurance adviser. The property manager reviews the gaps with the adviser and decides what is accepted.

## Who starts the work, and when

A property manager, or the property administrator working for one, starts it when new certificates come in from vendors, or on a set date each quarter to check the whole roster. The assistant needs the requirement sheet your team has already approved. It does not write one.

The property manager decides. The insurance adviser is the person the manager reviews each gap with before any certificate is accepted.

## What they supply

- **The requirement sheet:** the coverages, minimum limits, limit bases and extra terms your team has approved, by type of vendor, with who approved it and when.
- **The vendor roster:** each vendor's name, type of work, the properties it serves, whether a certificate is on file, and a contact.
- **The certificates,** pasted or typed in as text, one per vendor, with any endorsement pages supplied.
- **A few settings:** today's date, the certificate holder wording you require, how many days ahead to flag an expiry, the names of the portfolio and the sheet, and the reply date for requests, if you set one.

No connection to email, a document system or any insurer is needed, and none is asked for. The assistant never asks for a password or a login code.

## What comes out

One check in nine parts, in a fixed order:

1. **The basis:** the sheet used, who approved it and the settings.
2. **Vendors at a glance:** certificate on file or not, items to review, documents to request, earliest stated expiry.
3. **The field comparison,** vendor by vendor.
4. **Every stated expiration date,** soonest first.
5. **Missing documents.**
6. **Questions for the insurance adviser,** with endorsement wording quoted as written.
7. **Draft requests,** one per vendor with something missing, marked as not sent.
8. **What was not checked.**
9. **A blank decision line** for the property manager.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/), where the vendor file should show what was asked for and what came back. It sits beside [vendor renewal review](https://fullypowered.ai/workflows/vendor-renewal-review/), which looks at a contract's renewal terms, not its insurance paper.
- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), where the team keeps records of what it checked and when.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), for the routine of chasing renewals so nothing quietly lapses.
- [Real estate](https://fullypowered.ai/industries/real-estate/), where one manager may have cleaners, lift companies, landscapers and roofers across many buildings.
- [Construction](https://fullypowered.ai/industries/construction/), where a main contractor collects certificates from trades before they start on site.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where maintenance vendors are on site for shutdowns and repairs.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where certificates have been filed for years and nobody has laid them beside the requirements lately.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when new buildings or sites bring a wave of new vendors.

It is not a safety review of a contractor; [contractor safety prequalification](https://fullypowered.ai/workflows/contractor-safety-prequalification/) does that. It does not review your own business policies; [business insurance renewal review](https://fullypowered.ai/workflows/business-insurance-renewal-review/) does that. This one reads vendors' certificates against your sheet.

## What has to change for your company

- **Your requirement sheet.** Bring the one your team and adviser have approved. The workflow template will not invent minimums.
- **Your vendor types.** Name the types on your roster so the right lines of the sheet apply to each vendor.
- **Your certificate holder wording,** exactly as you want it to read.
- **Your expiry window.** Thirty days is the default.
- **Who you review with.** Name the insurance adviser and who stands in.
- **Which endorsement copies you ask for.** The default asks for a copy whenever the certificate marks additional insured as shown.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which documents the assistant may read.

The workflow template gives no insurance advice and no opinion on whether any cover is adequate or any wording works. It declines those questions and names them for your adviser.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026, in a second run made by the model that revised it; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a few vendors whose certificates your manager already knows well, plus cases written in advance with expected results: a limit below the sheet, a policy that has expired, a vendor type the sheet does not cover, a certificate for a differently named company, endorsement pages listed but not supplied. The property manager checks every field and every date against the certificates before anyone relies on the result. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Contractor safety prequalification](https://fullypowered.ai/workflows/contractor-safety-prequalification/)
- [Business insurance renewal review](https://fullypowered.ai/workflows/business-insurance-renewal-review/)
- [Vendor renewal review](https://fullypowered.ai/workflows/vendor-renewal-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
