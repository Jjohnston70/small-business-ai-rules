---
document_id: TNDS-PUB-005
title: "Verify Lite, the Pocket Verification Rule"
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
tags: [verification, citations, page-date, single-source]
notes: "Four steps, no tooling. For any AI-supplied fact headed into a decision or a document."
---

# Verify Lite

For any fact, number, rule, or price an AI hands you that is going into a decision or a document.

1. **Open the source.** Not the snippet, not the AI's paraphrase. The actual page.
2. **Read the date on the page.** Publication date, revision date, or "up to date as of." Write that date next to the fact. No date on the page means the fact is unconfirmed; find a dated source or do not use it.
3. **Prefer the publisher.** The agency, the regulator, the company's own page, the journal. A summary of the source is not the source.
4. **Label it.** One source: write "single-source" next to it. Two independent sources that agree: write "confirmed."

Paste into any AI prompt:

```
For every fact you give me: show the source URL, show the date printed on that page, prefer the original publisher over summaries, and say plainly if you could not find a dated source. Mark anything with only one source as single-source.
```

For regulations, ask for the eCFR page and its "up to date as of" line, and ask whether the rule has been amended. For prices, ask for the publisher's release date. For statistics, ask for the survey year and who ran it.

True North Data Strategies LLC | truenorthstrategyops.com
