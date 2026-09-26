---
document_id: TNDS-PUB-002
title: "Tool Routing for Subscription AI"
type: reference
domain: delivery
tnds_layer: delivery
version: "1.0"
owner: Jacob Johnston
organization: True North Data Strategies LLC
created: 2026-09-25
source: "Sanitized public edition of an internal TNDS asset, 2026-09-25"
status: draft
last_updated: 2026-09-25
review_due: 2027-03-25
supersedes: null
superseded_by: null
classification: public
authority: reference
approver: null
use_with: [claude, claude-code, cowork]
consumed_by: [ai-control-plane-solo]
corpus: none
related_assets: [TNDS-PUB-001]
tags: [tool-routing, chatgpt, claude, perplexity, gemini]
notes: "How to fill the routing table. Job first, tool second, data class decides the ceiling."
---

# Tool Routing

The table is built job by job, not tool by tool. Start with what you actually do in a week; the tool is the last column you fill.

## Filling a row

1. **Job.** Name the task the way you would say it out loud: "write the Monday customer update," "check a DOT rule," "summarize a vendor contract."
2. **Data class.** What is the most sensitive thing that will be in the box when you do this job? That is the row's class, and it sets the ceiling.
3. **Tool.** Pick the one that does this job best in your experience. If you do not have a view, run the same job in two tools once and keep the one that needed less fixing.
4. **Account.** Work. Always work. The only exception is a job that is genuinely personal.
5. **Output goes.** "You send it" means a human reads and sends. "Read before use" means the output feeds your thinking, not a document. "You approve every use" is for Confidential rows.
6. **Fallback.** Which tool takes the job if the first is down. Costs nothing to write, saves a morning.

## Picking tools without a vendor war

Any of the major chat tools drafts, summarizes, and rewrites well enough that the difference rarely matters for an owner-operator. Where they differ, in a way that changes the routing decision:

- Research with live sources: use a tool that shows the source and the date. Perplexity and Claude with search both do; check that the date shown is the page date, not the search date.
- Long documents you will query repeatedly: a tool built to hold sources (NotebookLM, Claude Projects) beats pasting the document into a fresh chat each time.
- Anything Confidential: the tool is whichever one passed the account checklist. Capability is second to settings here.

Do not assert tool features from memory when advising someone; features change monthly. Open the tool, look, then write the row.

## Routing table for a fuel distributor, example

| Job | Tool | Account | Data | Output goes | Fallback |
|---|---|---|---|---|---|
| Check a hazmat or hours-of-service rule | Claude with search | Work | Public | Read before use; open the eCFR page, note its date | Perplexity |
| Draft the weekly driver safety note | Claude | Work | Internal | You send it | ChatGPT |
| Summarize a new vendor contract | Claude Project | Work | Confidential, checklist passed | You approve every use | none, wait |
| Anything with rack prices from a paid feed | No AI tool | none | Licensed | Stays in the pricing sheet | none |

True North Data Strategies LLC | truenorthstrategyops.com
