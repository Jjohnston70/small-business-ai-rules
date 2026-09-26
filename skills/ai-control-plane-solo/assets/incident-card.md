---
document_id: TNDS-PUB-006
title: "AI Incident Card"
type: template
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
tags: [incident, kill-switch, template]
notes: "One card per business. Print it. The person who is not you must be able to find it."
---

# AI Incident Card

If something went into an AI tool that should not have, or an account looks compromised, do these in order.

| Step | Tool: __________ | Tool: __________ | Tool: __________ |
|---|---|---|---|
| Change password, end all sessions (path) | | | |
| Delete all chat history (path) | | | |
| Disconnect every app and integration (path) | | | |
| Revoke from the other side (Workspace or M365 admin path) | | | |
| Export my data (path) | | | |
| Vendor support contact | | | |

Then:
1. Write one decision-log row: what went in, when, which tool, what you did.
2. If it was Confidential customer or employee data, decide with counsel whether notification is required. Do not decide that alone.
3. Re-run the account checklist for that tool before using it again.

If a tool is down and you need to work: the routing table's fallback column says which tool takes each job.

True North Data Strategies LLC | truenorthstrategyops.com
